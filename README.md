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

### 3) Clone the repo to your machine

In the top right corner of your newly forked repo on your github account, find the "clone" button. Clicking it will populate a URL that you can copy and paste into the terminal to clone the repo. Your command will looks something like the following, populated with your github username.

```
git clone https://github.com/students_personal_github_account/microteaching.git
```

It should prompt download the repo to your desktop. You can take this opportunity to look around and check that it did so.

### 3b) Navigate to your repo

You have cloned your repo, and if you check your desktop, you can see that your repo exists! But wait--if you look at your command line, you're still simply on your desktop and not in the folder you just created. To descend one level deeper into your computer's file structure, into the microteaching folder now on your desktop, type:

```
cd microteaching
```

_NB: for more information on Unix commands, see [here](http://mally.stanford.edu/~sr/computing/basic-unix.html)._

### 4) Checkout onto a new branch, set upstream branch

To create a new working branch, type the following. A typical workflow involves working on a development branch and pushing major milestone changes to the main branch. "name_of_branch" can be whatever you want it to be.

```
git checkout -b name_of_branch
```

Now you want to set the upstream repo. This is the original repo against which you want to compare yours. While you can go on working all day editing the repo on your github account, you may want to keep your repo updated with the original user's repo so as to receive any new developments. As we will soon see, this is also essential so that git knows where to submit a pull request once we have made our own changes to the repo that we want to share!

```
git remote upstream add https://github.com/hunterwyork2/microteaching.git
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

Finally, to push your changes to your main remote (github.com) repo, type the following. 

```
git push -u origin name_of_branch
```

This should return a message like the following (here, my branch is named "hunter."):

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

By navigating to the above URL, you can follow the onscreen prompts to create a pull request! If a URL prompt does not appear, go to your repo online, and it should be there.
