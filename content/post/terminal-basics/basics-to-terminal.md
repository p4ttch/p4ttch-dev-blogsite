---
title: "Basics of Terminal"
date: 2020-11-10T21:29:12+02:00
draft: false
tags: ["CLI"," CMD","StudyNotes","Terminal", "Command line"]
categories: ["Terminal"]
---

# Introduction
Welcome to command line basics. In these notes I will cover some tips and tricks to learn the basics of the terminal in Windows command promt (cmd) and bash. Mostly how to navigate in and out of folders. Make new folders. And list folders.
1. cmd 
2. bash

# 1. CMD
## Command list

<!-- |Command|What it do|Link to section| -->
|Command|What it do|
|---|:---:|
|dir|lists directories|
|cd| change directory|
|mkdir|make directory|
|help| shows list of commands and descriptions|
|cls| clears the screen|


## In Practice
Lets start by opening the terminal / command line.
press windows key + R . This brings up the run window. Type in cmd and pushe enter.
That will bring up the command prompt or cmd.

<!-- It should look something like this -->
<!-- <insert img> -->

It should be showing 
`Microsoft Windows [Version 10.0.18362.1139]
(c) 2019 Microsoft Corporation. All rights reserved.

C:\Users\{Your PC's user name}>`

### dir
First we will type  `dir` and push enter
This is the command to list directories, AKA folders. You should get a long list. With dates time stamps. a few <DIR> tags and the name of the file or directory.

### cd
To go back a folder, we type `cd ../`  cd is the command for Change Directory. and the "../" means we move up a folder, we can chain them to move up two or more folders . example `cd ../../` would go up 2 folders.

I am in C:\users. I want to go back to p4ttch and documents so i will type `cd p4ttch/documents`.
A tip, you can start the command `cd` space and the first letter of a folder you want to go into. And push tab. It will auto complete the name of the next folder / directory it thinks you want to enter in alphabetical order. So just keep pushing tab until you hit the folder OR you could type the first few letters to narrow the list down.

you can then type / and start it again until you have your file path you wish to enter.

### mkdir
