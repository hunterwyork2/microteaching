# Overview

Git repositories (repos) are a useful place to store code, whether working by yourself or with others. A key feature of the collaborative component of the git workflow is called a *pull request*. A pull requests assumes that you have worked on the same repository as the code owner, made some changes, and want to share your changes with the code owner. 

## Step-by-step instructions

### 1) Fork the repo

In the top right corner of this page, click fork. This will create a repo in your github account matching the one existing here. Once it's in your github account, you will want to clone it onto your machine so you can make the changes you'd like to.

### 2) Navigate to your desktop on the command line

To clone the repo, open the command line on your machine. This is called "terminal" on Macs and "cmd" or "Command Prompt" on Windows. Git comes preinstalled on most Mac releases, but you may have to install it yourself on Windows. To do so follow this [link](https://git-scm.com/download/win). 

In the command prompt, you want to navigate to the location where you want the repository to live. For now, lets work on your desktop. 

To begin, navigate to your desktop. Replace "(username)" with your username. This is what you use to login to your machine, not to Github.

**In Windows**
```
cd C:/Users/(username)/Desktop
```
Using my username:
```
cd C:/Users/hyork/Desktop
```

**On Macs**
```
cd /Users/(username)/Desktop
```

### 3) Clone the repo

Type the following

```git
git clone https://github.com/hunterwyork/microteaching.git
```

It should prompt download the repo to your desktop. 

### 4) Checkout onto a new branch

To create a new working branch, type the following. A typical workflow involves working on a development branch and pushing major milestone changes to the main branch. "name_of_branch" can be whatever you want it to be.

```
git checkout -b name_of_branch
```


### 5) Make changes

In the repo, there is a file _feedback.txt_. Open this using whatever text editor you prefer: textedit, sublime, wordpad, etc. Type 1-2 sentences containing your reaction to the teaching session.

### 5) Commit your changes

Once you want to save your progress, you can commit your changes locally (on your machine) and within github. To commit them locally, start by adding items to your commit. Since you only have one item in the repo, we can use shorthand to add everything to the commit using a period.

```
git add .
```

Now, add a one line description containing the changes in your commit. I'm going to say that my commit "updated feedback file."

```
git commit -m "updated feedback file"
```

### 6) Push your changes

Finally, to push your changes to your main repo, type the following. If all goes well, you will be prompted to initiate a pull request.

```
git push -u origin name_of_branch
```

This should return a message like the following:

```

> hyork@opr-hyork-mbpro microteaching-1 % git push -u origin hunter
git: 'credential-manager.core' is not a git command. See 'git --help'.
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 449.04 KiB | 24.95 MiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'hunter' on GitHub by visiting:
remote:      https://github.com/hunterwyork/microteaching-1/pull/new/hunter
remote: 
To https://github.com/hunterwyork/microteaching-1.git
 * [new branch]      hunter -> hunter
Branch 'hunter' set up to track remote branch 'hunter' from 'origin'.

```

### 7) Create a pull request

By navigating to the above URL, you can follow the onscreen prompts to create a pull request!
