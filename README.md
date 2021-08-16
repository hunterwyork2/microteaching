# Overview

Git repositories (repos) are a useful place to store code, whether working by yourself or with others. A key feature of the collaborative component of the git workflow is called a *pull request*. A pull requests assumes that you have worked on the same repository as the code owner, made some changes, and want to share your changes with the code owner. 

## Step-by-step instructions

### 1) Navigate to your desktop

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

### 2) Clone the repo

Type the following

```git
git clone https://github.com/hunterwyork/microteaching.git
```

It should prompt download the repo to your desktop. 

### 3) Make changes

In the repo, there is a file _feedback.txt_. Open this using whatever text editor you prefer: textedit, sublime, wordpad, etc. Type 1-2 sentences containing your reaction to the teaching session.

### 4) Commit your changes

Once you want to save your progress, you can commit your changes locally (on your machine) and within github. To commit them locally, start by adding items to your commit. Since you only have one item in the repo, we can use shorthand to add everything to the commit using a period.

```
git add .
```

Now, add a one line description containing the changes in your commit. I'm going to say that my commit "updated feedback file."

```
git commit -m "updated feedback file"
```

### 5) Push your changes

Finally, to push your changes to your main repo. 

```
