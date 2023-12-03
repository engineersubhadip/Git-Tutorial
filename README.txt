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

git rm --cached <file> -> This removes file from the Staging area to the working area.

git commit -> registers staging changes to a commit. (Then press esc+:+wq+enter)

git log -> Lists down all the commit history of the Repository. (To exit out of it press "q").






