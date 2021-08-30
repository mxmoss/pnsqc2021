# Prerequisites

## 1) Install the git client on your local computer.

Go here: <https://git-scm.com/book/en/v2/Getting-Started-Installing-Git>

Install the precompiled Git tools for your operating system

### a) For Windows 
  <https://git-scm.com/download/win>
  
### b) For Linux

    sudo dnf install git-all
  
### c) For MacOS
  run git from the Terminal the very first time.

    $ git --version

  if that doesn't work 
  <https://git-scm.com/download/mac>

Choose all the defaults...

Except: Choose whatever editor is most comfortable for you 

## 2) Sign up for a github account

Sign up here on github: <https://github.com/signup?source=login>

Use a real email address, so you can get the email confirmations & launch code

Follow the instructions for signing up 

Suggested signup choices:
- Just me
- Student
- Collborative coding 
- Automation and CI/CD
- Security 
- Project Management 
- Community
- "Continue for free" 

You can play with the hello world repo project if you want 
<https://guides.github.com/activities/hello-world/>


# Exercises

## Ex. 1) Fork the workshop Repo from my account on Github 

Go here:
<https://github.com/mxmoss/pnsqc2021>

Click on the [Fork] button

Explore the fork of the project in your repo 

## Ex. 2) Clone the project locally

### a) Open a terminal to use the git command line

To start a Command Prompt or PowerShell in Windows:

    [ctrl]+[Esc] | Cmd | [enter]

To open a terminal in macOS:

    [Command]+[Space] | Terminal.app | [Enter]

From the command prompt, type 'git' and press return to verify that git is installed

### b) Clone the project onto your computer

    git clone https://github.com/<yourgithub>/pnsqc2021.git  

where <yourgithub> is your github account name.

eg: my account name is mxmoss.

    git clone https://github.com/mxmoss/pnsqc2021.git 

You should see something like:

    Cloning into 'pnsqc2021'...
    remote: Enumerating objects: 4, done.
    remote: Counting objects: 100% (4/4), done.
    remote: Compressing objects: 100% (3/3), done.
    remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
    Unpacking objects: 100% (4/4), done.
    Checking connectivity... done.

### c) Verify that the files are local

//View the files in the directory

    dir pnsqc2021 

//Move to the directory with the repo

    cd pnsqc2021

//Try some git commands:

    git (with no parameters) 
    git help -g
    git help -a
    git status 
    git config 

//Set configuration if necessary. Do this only if user.email or user.name are empty

//To check:

    git config --global user.email
    git config --global user.name
	
//To set: 

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"
  
//While we're talking about configuration, let's create a Personal Access Token (PAT)

//In the upper-right corner of any github page, click your profile photo, then...

//Settings | Developer Settings | Personal access tokens 

//Type in "pnsqc 2021 token" for the description

//Treat this token like a password

## Ex. 3) Add a new feature to the project
//Make a branch so we can work safely

    git checkout -b my-feat1

//Create the file learnings.txt 

### Windows: 

    notepad learnings.md 
  
### Linux: 

    vim learnings.md
	
//Linux: nano learnings.md 

### MacOS: 

    vim learnings.md 

Add the following text:
- What did I learn from the workshop?
- Did I have any un-met expectations?

Save and exit editor

//Verify that you have created the new file 

    git status

//Add the untracked file to the repo

    git add index.md 
	
//alternatively, add _all_untracked files 

    git add .

//Commit the changes to the local repo 

    git commit -m "my first commit"

//Push the changes to the remote repo

    git push -u origin my-feat1

//You may need to enter your github username

//Enter the previously generated token (PAT) in the password field.

## Ex. 4) Pull requests
//In this exercise we issue a pull request to an upstream repository
First, fork the repo
(/img/GitForkARepo.png)

Create a new file called "learnings.txt".  Enter at least one thing you've learned during today's workshop.
(/img/GitOpenPullRequest.png)

Create this file on a new feature branch (see illustration)
(/img/GitAddingProposingAChange.png)

Click on the project, and notice that it's prompting you to create a pull request.
(/img/GitAddingProposingAChange2.png)

On my repo, I get a notification of the pull request.
(/img/GitPullRequestNotification.png)
(/img/GitRespondToPullRequest.png)
Normally, I would test your changes and review them. 
In this case I will accept the pull request.
(/img/GitPullRequestMerge.png)
Since many of you are submitting the same file, I will see a merge conflict.
(/img/GitConflicts.png)
I have to manually reconcile any conflicts.
(/img/GitReconcileConflicts.png)


## Ex. 5) Github pages 
// Publish your repository on Github Pages



// Configure the repo to publish the main branch

// Optionally choose a markdown preprocessor

// View the page


## Links 
- [GitHub](http://github.com)
- [GitHub Cheat Sheet](https://github.com/tiimgreen/github-cheat-sheet)
- [Awesome Lists](https://github.com/sindresorhus/awesome)
- [Generating an access token](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token)
- [How to use access tokens](https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations)
- [using OAuth tokens for github automation](https://docs.github.com/en/github/extending-github/git-automation-with-oauth-tokens)
- [Markdown for Github Pages](https://www.markdownguide.org/basic-syntax ) instead of HTML
- [Collaboration exercise](https://github.com/git-guides/git-add#examples-of-git-add)
- [Confusing terms in git](https://levelup.gitconnected.com/confusing-terms-in-the-git-terminology-c7115d6febc7)
- [Getting started with open source](https://dev.to/roligautam/how-to-make-your-first-contribution-to-open-source-a-beginner-s-guide-2cni)
