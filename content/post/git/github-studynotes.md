---
title: "Github Studynotes"
date: 2020-02-05T15:08:29+02:00
draft: false
tags: ["Git"," Repo","StudyNotes"]
categories: ["Git"]
---

# Introduction
Disclaimer : I work on a windows computer, so some of the steps might not line up for mac or linux users.
In this article I will cover a few senarios I've had experience with so far. 
1. Creating a New Repository AKA Repo. And pushing a new or current project into git.
2. Cloning an existing project repo.

# 1. Pusing a new project to git
## Create the repo
First step is to go make a new Github repository. 
Go to github.com and sign up / or login. 
Then at the top right there is a little plus arrow.  We are going to select "New Repository"
Give it a name. I'm calling mine "example-repo". Keep in mind, if you have an existing project you want to push. The folder on your computer and the git repo must have the same name. I'll be making a folder called example-repo in the next section.

And I'm setting mine to private for this. I'll delete the repo at the end. 
Going to leave the rest of the options blank and click 'Create repository' at the bottom.

This will make the new repo and you will see the Quick setup page with lists of commands on how to get start.

## Link the folder on your computer
I am using git-bash as my terminal window to run my git commands. There are other ways to do this
1. The Terminal in VS code. 
2. Windows command prompt
3. git-bash
4. Git plugin for VS-code
5. Visual Studio has it's own git managment tools

In bash we go to the folder. So for me it's C:\_personalprojects\example-repo. 
I have put an html hellow world into the folder with the name index.html for this demo. 

now i type `git init` , this will initialise this folder as a git repo. And now i get the message result : 
"Initialized empty Git repository in C:/_personalprojects/example-repo/.git/"

If we check the folder. We will have a hidden .git file. If you are looking in the folder. you can click View in the options at the top and then check the box "hidden items" or in bash you can type `ls -al` to see all the items in the directory.

Now we need to ADD our html file with one of the folloing commands: 
`git add .`

`git add -A`

`git add -all`

`git add [filename]` in our case `git add index.html`


I preffer to use `git add .` because it's the shortest. And even if we only have 1 file it still gets added with the add all commands. 

Now we need to commit our added files, and commits normaly have a commit message attached which explains what happened in the update. This is to help the other developers and your future self.
`git commit -m "first commit"` 

I am skipping the command in the git docs `git branch -M main`.  The branch should already be set to master, and this will make the main branch named main. 

Now we add the origin. This is the step that links our commited code to a repository on github. The git repository where the code is stored becomes the source of truth for the code. Thats the origin of the master copy of your code. So update this often.
`git remote add origin https://github.com/[Your Github User Name]/example-repo.git`

Then lastly we can push our code up to the master branch. 
```   
    git push -u origin master
```

I got an error during this demo, If you get an error. Always read it, try google if you dont understand it. Or try what the error code suggests to solve the problem.

"fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use"
```
    git push --set-upstream origin master
```

So i ran this command . i got another error
"git push --set-upstream origin master
Fatal: HttpRequestException encountered.
"
It connected, but had an authorisation error because i have multiple git users on this laptop. So i had to specify which user i wanted to use, and type in the credentials. Once that was done. it worked.

`Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 382 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/p4ttch/example-repo.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.`

Now we can go to Github in the browsers and take a look at what we commited.

# How To Github for noobs

These study notes come from LearnCode.academy's youtube video 
Link : https://www.youtube.com/watch?v=0fKg7e37bQE 

## Create the repo
First step is to go make a new Github repository. 
Go to github.com and sign up / or login. 
Then at the top right there is a little plus arrow.  We are going to select "New Repository"
Give it a name. I'm calling mine example-repo. And I'm setting mine to private for this. I'll delete the repo at the end. 
Going to leave the rest of the options blank and click 'Create repository' at the bottom.

### Command 1 - git clone
Then the first command is git clone. This is to link up the git repository (repo) with the project on your computer. 

example  

`git clone https://github.com/p4ttch/hello-world.git`

#Command 2 - git status
This is used to check the status on the git repo, and if it's in synch with your local project. 
It will show what files are new in your local project that git doesnt know about yet.
It will show what files git has that you dont know about yet and need to pull
And any modified pages that dont match the gits version.

#Command 3 - git commit
using `git commit` will put your changes into staging. and set your files as commited.
it's best to add a helpful message related to the changes you made with this commit. the full command is 
`git commit -m 'custom message here'`

if by chance you forgot to use the -m 'msg' with the command. the terminal will bring up a screen for you to insert a multi line commit message. Actually usefull if there where multiple tasks in 1 commit.

Once you have made your message. To get out of this screen and back to normal terminal
Press Esc, then `:wq` + enter

#Command 4 - git pull

#Command 5 - git push

#Command 6 - git add
there are a few different versions of this
we can add 1 specific file with `git add [filename]`
we can add all our work too with 1 of the following

```
    git add .
    git add -A
    git add -all 
```
 
When you use the `git push` command in command line. This will try push your changes to the git repo. But first it will check if you have permission to do so.
If you havnt been authenticated yet it will bring up a window asking you to login.
Alternitavely it will bring up a request in comand line for user name and password. 

#GITHUB PULL REQUEST, Branching, Merging & Team Workflow
these study notes come from LearnCode.academy's youtube video 
Link : https://www.youtube.com/watch?v=oFYyTZwMyAg

#git branch
- lets you see all the branches related to the project

#git branch [name]
creates a new branch with the specified name.
`git branch feature1` will create a new branch named feature1
This creates a copy of the master branch

#git checkout [branch name]
so to get into our new branch , in the terminal use the command
`git checkout feature1` 

#How to handle Pulls Requests



#Other good github guides
Link : https://rogerdudler.github.io/git-guide/