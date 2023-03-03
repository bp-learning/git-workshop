# git-workshop

## Why do we need version control?
Have you ever worked on a big puzzle or a drawing that took a long time to finish? And maybe you made some mistakes along the way or wanted to try different things to see what looked best? Well, programming is kind of like that too. When people write computer programs, they often have to work on them for a long time and make lots of changes.

That's where Git comes in! Git is like a special tool that helps programmers keep track of all the changes they make to their programs. It's kind of like a big notebook where they can write down what they changed, when they changed it, and why.

Similarly, Let’s say you create a project and have worked on it for over a month. While adding a new feature, you realize that something you did a week back won’t allow your new feature to work properly. You decide to revert those changes but aren’t sure if you have made similar changes in other files as well.

What if there was a way for you to identify what exact changes you made and where in your code you made them? That’s where version control can help you out.

## Prime Reasons
- Keep track of changes to the codebase
- Ease in collaborative work
- Showcase your code to outside world( helpful in interviews)

## What is Git?
- Git is a distributed version control software. 
- a complete copy of the entire codebase will be available on every contributor’s computer; we can also call this codebase a **local repository**.
- Git tracks the local repository, maintains a record of all the changes that occur within it.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/1024px-Git-logo.svg.png" width="300">

## Git is distributed version control

<img src="./git-1.png" width="500">

## How to install GIT?

https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

## How to check whether git is installed successfully in your system?

Open command prompt or terminal and type
```
git --version
```

## git config

Our main goal is to set our credentials that will identify our contributions and changes in the project source code. Doing so will help us identify and differentiate between the changes made by various contributors.

## Setting our email and username for Git
We will set up our name and email globally for Git by using the following commands:
```
git config --global user.email "tom_curise@gmail.com"
```
Similarly, we will also set up our username too:
```
git config --global user.name "Tom Cruise"
```

You can verify your configurations for setting up the email and username by typing in the commands:
```
git config user.email
git config user.name
```

## Creating a New Project With Git
Lets create a folder first
```
mkdir sample_project
```
Go inside the folder
```
cd sample_project
```
Lets open this folder in vscode or any other IDE of your choice
and create a file called Test.java

```
-- sample_project
|---- Test.java
```
Now we a folder and a file created in it, let initialise this folder into git repository.

In Terminal, type the command
```
git init
```

- The git init command simply creates an empty repository.
- What git init does, however, is create a .git directory. 
- The .git directory will contain all the metadata that Git will require for tracking the project.

- The subdirectory .git will contain several files and more subdirectories that Git will use to keep track of changes in the project.

Usually .git directory is hidden, and its recomended that we should not touch it, if we want git to work perfectly for your project

## git status command
Type git status in the terminal
```
git status
```
Output
<image src="git-2.png">

The Red marked files indicates that there are changes in the directory. In our case, a new file is added which is not yet commited in git repo.

## Let make this file ready for commit by using git add
In your terminal, type
```
git add .
git status
```
Output
<img src="git-3.png">

## Now your changes are ready to be commit, Let commit
Type on your terminal
```
git commit -m "Test file created"
```
Output
<img src="git-4.png">

## Let check git status now
```
git status
```
<img src="git-5.png">
We have successfully comitted our first change

**Note: Always put good comment message while commit**

## Lets do few more change
<img src="git-6.png">

## Lets check the status now
<img src="git-7.png">
Now you can see the file is modified and there are changes we can commit.

Before commit we have to make the changes ready for commit. This process is called moving the changes to staging area.

## Moving changes to staging area
```
git add .
git status
```
<img src="git-8.png">

## Commit the new changes
Since we have the code in staging area(Code ready to be commited). Lets commit it using git commit
```
git commit -m "Hello World Program added"
```
and then check the git status
```
git status
```
<img src="git-9.png">

## Lets check what are the changes we have done so far using git log
```
git log
```
<img src="git-10.png">
