# Git And Github Masterclass

- VCs (Version Control System):Git, Mercurial, Subversion
- mercurial : 2010
  -git : 1. linux 2. branching
- NS3 / NS2 (software): network simulator, submarine , data packets, how to simulate, mercurial used

# Some Basics Commands

- git : to show git commands
- git install : to install git in your system
- git init : git start tracking or initialized the project

# .git

hidden folder created

- `ls -a`: to get all files and folders lists
  - index , objects inside **.git** folder
- `git add <file.txt>` : star tracking the particular file
- `git add .` : start all file tracking (added Index) (A) and added into staging state
  git status - to see the staging and unstage file
- `git commit -m"first init"`: create checkpoint , saved area or snapshot of some features / code
- git diff : to show difference from previous commit to what are the changes happen till new commit
- git log : to give commit history : author , date, message , commit id (which git track the file)
  that is keep in **.git** (objects)
- `git cat-file -p [commit id] `: to read the commit
- `cat some.txt` : to read the file text
- `git cat-file -t [commit id]`: to say type of file

- `git reset <commit id>` : to reset head and it brings the added files into changes
- `git reset --hard<commit id>`: hard reset that remove all the changes

## hash key in commit

basically git take all our code and hash it with sha1 algo to make hash

### Assignments OnBoarding Documentation that written in Assignments folder
