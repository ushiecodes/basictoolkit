class 1: 31/07/25

git init - will initalize an empty git repository in the specified folder with .git extention (it is a hidden path)

intermediate area - where the current edits of file(s) are not tracked by .git (Untracked)

staging area - where your current edits will be tracked but not committed (Modified)
git add {filename}

commit - takes a snapshot at a particular time by a particular person (author) and these commit(s) are unique
git commit -m "your message"
make sure your commit messages are meaningful
example: a very specific message saying you added a function which does this etc

when initial git commit - it keeps track of change of files at which time by whom
it will ask you 'please tell me who you are' - need to setup credentials

run the git commit command again, when succesful you will get:

PS C:\Users\Utkarsh Kamat\Documents\.vscode\ids241lab> git commit -m "modified readme.txt  with git commands"
[master (root-commit) b7e6c6f] modified readme.txt  with git commands
 1 file changed, 6 insertions(+)
 create mode 100644 readme.txt

to see what the actual commmit looks like, we use:
git log

every git commit has a unique hash, if you want to go to a specific commit, you need to know that specific commits hash (HEAD -> master)

committing it to a remote version control system - using github

git config --global user.name "name"
git config --global user.email "email"

credential manager

git add origin "reposistory link" intermediate phase between your local repository and remote repository (github)
git remote -v : will show u the link to the commits

to push the intermediate commit to staging area:
git push --set-upstream origin master

#class 2 - 01/08/25

adding multiple files using git add
git add .

adding only a subfolder using git add
git add "foldername"/

.gitignore - will ignore any file you dont want to push on git

example: 
file - secret.js (needs to be in gitignore)
gitignore - mention the file name
push the commit and it wont show the ignored file

mention the name of the file or use "foldername"/ to indicate that this is a folder and needs to be ignored
basically if you are committing multiple files except a few in that selection, adding the name or subfolder in gitignore will not push it to the repository

