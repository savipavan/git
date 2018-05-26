# git
Git 
---
cat ~/.gitconfig

git config --global-list

git config --global user.name "savipavan"
git config --global user.email "savipavan@gmail.com"

git config --global --list

cat ~./gitconfig

#set additional properties
git config --global core.editor <<notepad++>> <<VIM>> <<EMACS>>
#Another configuration option
git config --global help.autocorrect 1
#Set Color to output in Command Line
git config --global color.ui auto

#To check all above configurations
git config --global --list
cat ~/.gitconfig

#update user name information
git config user.name "pavankumar"

git config --global --list

#remove updated user.name
git config --unset user.name "pavankumar"

git config --list

vim .git/config

#Creating A Local repository
mkdir gittest
#turn in into local repository
git init
ls -la
echo "Hello, Git" > README.txt
# Check the status
git status
#Add the file in to Staging Repository
git add README.txt
git status

#git commit
Added Readme.txt
#check the history
git log

#update README with second line
git status

#Add all modified files
git add -u

#commit the update with inline
git commit -m "updated README.txt"

git log

#Check the differences in both commits
git log

git diff <<FirstLogNo>> <Second Log No>
git diff dd6819..a15ec6

git diff HEAD~1..HEAD
git diff HEAD~1..
touch file1.txt file2.txt
git status
git add -u  #it will add only updated files"

#Add files
git add file1.ext file2.ext
git add -A

git commit -m "Added new files"
git log
git diff HEAD~1

2.4Staging changes as multiple commits
----
vim file1.txt
	"Adding some code here"
	:wq!

vim readme
"updated new changes"
:wq!

git status
git add file1.txt

git status
git commit -m "fixed bugs#123"

git add README.txt
git commit -m "Fixed typo in Readme.txt"

2.5Deleting and renaming files
-----
rm file2.txt

git add -u
git status
vim file3.txt
git status
git add file3.txt
git status

#change the file name
mv file1.txt new_file_name.txt

git status
git add -A
git status

git commit -m "Reorganize the feature"
git status
git log

2.6Undoing changes to the working copy
vim README.txt
	Remove all existing lines
		
git checkout README.txt
git status
cat README.txt

vim README.txt
<<Delete>> all the contents
:wq!

#remove the file
rm new_file_name.txt

git status

#reset the settings
git reset --hard

#git status

2.6Undoing changes to the working copy

git log
git reset --soft HEAD~1
git log
git status

git commit -m "reorganize"
git status

git log
git reset --hard HEAD~1

git status

git log

2.8Cleaning the working copy

touch temp1.txt temp2.txt
git status


git clean
git clean -n
git clean -f
git status

2.9Ignoring files with .gitignore
					---
mkdir logs
touch logs/log.txt

vim .gitignore
logs or /logs/*.txt
/logs.*log
/logs
:wq!

git status
git add .gitignore
git commit -m "Added .gitignore"
git status
git log

3. Working Remotely with Git
-----
- Cloning a remote repository
- Listing remote repositories
- Fetching changes from a remote
- Merging changes
- Pulling from a remote
- Pushing changes remotely
- Working with tags

3.1 Cloning repositories
--
git clone https://github.com/jquery/jquery.git
