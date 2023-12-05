`git init` -> Powers your folder to be managed by GIT. It also creates a .git folder.
              that has all the relevant logic to manage to versions of your project.

`working area` -> There can be a bunch of files that are not currently handled by GIT.
                  It means the changes to be done in those files are not managed by GIT yet.
                  A file which is in working area is considered to be in the Staging area.
                  When we do git Status we find a bunch of un-tracked files, then these are
                  actually called to be in the working area.

`Staging area`-> It is going to tell you what all files are going to be part of the next  version that we will create. This is the place where GIT knows what changes to be done from the last version to the next version.

`Repository Area` -> This area actually contains the details of all your previous registered versions. And the files in this area, GIT already manages them and knows their version history.

`commit` -> It is the particular version of the project. It captures a snap of the project's staged changes and creates a version out of it.

git add <file> -> This moves files from working area to the Staging area.

git restore --staged <file> -> This moves the changes from the Staging Area to the Working Area.

git commit -> registers staging changes to a commit. (Press "i" to enter the commit message and then press esc+:+wq+enter)

git log -> Lists down all the commit history of the Repository. (To exit out of it press "q").
In windows we don't need to press any such thing.

git restore <file>-> It removes all file changes from the working area

git commit -m "Commit Message to be written" -> Shortcut to write Git Commit Message.

git push origin master -> Using this we can push the changes from the local git repository to the GITHUB repository.

git remote rm <remote name> -> This deletes the connection between the local and the GitHub Repository.

git remote rename <oldname> <newname> -> This renames the old connection.

git add <file1> <file2> ... -> This command will add multiple file changes in the Staging Area.

git add . -> If we do not want to add all the file names manually.

git pull origin master -> If we want to download the updated file changes from the GitHub Repo Branch to your local machine

<!-- * Recommended Practice -->
1. Git Pull
2. Make Changes
3. Git Add <file>
4. Git commit.
5. Git Push


//* Scenario :- We have a file already committed. In that file whatever changes we make, that changes are basically done in the WORKING AREA. In the working area if we do "git restore <file>" then all the changes we make from the working area vanishes.
But, If we want those changes to move from working area to STAGING AREA, we need "git add <file>", this will move the file from the WORKING AREA to the STAGING AREA. And from the STAGING AREA, we can do "git commit".
If we want those changes again to be moved from the STAGING AREA to the WORKING AREA we can do "git restore --staged <file>".
Therefore only those changes become part of the commit which are in the STAGING AREA.

Difference between "git rm" and "git restore" -> If we want to move the whole file back to the working stage, we do "git rm". Otherwise if we just want the changes to be shifted to the working or staging area we do "git restore".

How to check the Difference between two commit -> Get the first commitID and the second commitID. Then do,
"git diff commitID1 commitID2"


All the Changes that we are making right now are in our local repository (in our computer). If we want to connect our local repository to the GitHub Repository we need (git remote add origin https://github.com/gautoma/Git-Tutorial.git).


Merge Conflicts occur :-> When 2 or more people are tying to make changes at the same part of the code.
Merge Conflicts are very common Scenario

Stashing -> If we have some piece of code which we do not want it to be a part of the next commit, we can use stashing.
-: Procedure :-
1. Whatever file we have push it into the Staging Area.
2. From there do "git stash". This will move the file from the Staging Area to the Stash.
3. If we want to see all the list of the stash file we can do "git stash list".
4. If we want the file from the Stash back to the Staging Area we can do "git stash apply".

git stash show stash@{stashNumber} -> To see how many changes are there in the current stash

How to store changes for the untracked file -> git stash --include-untracked
OR, we can push the file in the Staging Area and from there do 'git stash'.