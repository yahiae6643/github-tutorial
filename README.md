# GitHub Tutorial   
_by Yahia Elhag_

---
## Git vs. GitHub
![GIT](https://raw.githubusercontent.com/yahiae6643/github-tutorial/master/Git-Icon-1788C.png)
###### `Image source: https://git-scm.com/downloads/logos` 
**_Git_** is defined as the system which is primarily used to give the user control of his versions _(Version Control)_. Specifically, git gives you the ability to **save changes of your file as previous versions over time**.  
> You can refer to your previous changes easily if you have a problem with your current project or want to use previous code in your project in order to improve it.  
> You can also remove these changes if you believe they are not needed in your history.  

![GITHUB](https://raw.githubusercontent.com/yahiae6643/github-tutorial/master/GitHub-Mark.png)

###### `Image source: https://github.com/logos` 
  
Github is a website used to post your projects and their previous versions for everyone to see. Since it is based on _Git_ (**Git** in **Git**hub), you can refer back to your projects for the sake of improvement, removal, or fixing errors with your current file. However, the main difference between the two is that it is also used to **easily collaborate with one or more users on one or multiple projects**.
> Users go through a very short and easy process in order to collaborate with others, which would be taught later in the tutorial!  
> Collaborations are usually for adding suggested features or fixing bugs on one project, but they can be used for so much more!

---
## Initial Setup
###### Creating and setting up a github account is pretty straightforward, lets begin!

NOTE: Cloud9 link is [c9.io](c9.io)

**Step One**: Go to `https://github.com/`. Here is the website: [_Github_](https://github.com/)  
* You have found the website successfully if you reached a site that looks like this:

![GITHUB_PAGE](https://raw.githubusercontent.com/yahiae6643/github-tutorial/master/github_screen.png)

**Step Two**: Within the front page of github, you are presented with a white box that states for you to choose a *Username*, *Email (Can be either your **personal** email or **school** email)*, and a *Password (Must be greater than 7 and less than 15 characters for security reasons)*

* Soon after creating your account, it will be unverified as a user (you would need to access your email to verify it) and you will be given two plans, **Free** and **Developer**. 

![Plans](https://raw.githubusercontent.com/yahiae6643/github-tutorial/master/plans.png)

> Choosing the free plan has no consequences, so don't worry if you chose it  
    
* You will then be given to choose what projects you want to see based on your interests
    * It isn't very important, so you have the ability to skip it

* **You have successfully created an account, but you need to connect it to your cloud9 account (IF YOU HAVE ONE) to create and send your projects**
    
###### The process of connecting your github account to cloud9 is easier, so lets start!

**Step One**: Access the main page of cloud9 and log in with your github account **(If you don't have a c9 account, make one)**.
* There is a possibly that creating a c9 account can cost money, **so the steps below might be similar to other online websites you use such as _Codiad_ or _Shiftedit_**

**Step Two**: Press the _gear icon_ on the top right of the screen for a list of settings and press **_SSH Keys_**
>SSH Keys (**S**ecure **S**ocket S**h**ell) is a network protocol that gives you access to a remote area, such as _Github_, from another area without typing your password and username. Without a SSH Key being linked between your github and cloud9, you won't have the ability to send and take projects from your c9 to github without typing your password and username, which is really inefficient  

**Step Three**: Copy the private git SSH repository

![c9 SSH](https://raw.githubusercontent.com/yahiae6643/github-tutorial/master/c9.png)

**Step Four**: Go to Github and access your settings on top right corner
    * Press _SSH and GPG keys_ and create a new SSH key, which brings you to two text boxes. Paste your SSH in the bigger box and type "cloud9" in the smaller text box. **Finally, press _Add SSH Key_**

> **The account has been finally set up, now for setting up your workspace!**
---
## Repository Setup


###### To start...
**NOTE**: A repository is a folder where you save both your files and file changes permanantly as previous versions of the project (until further modifications)  
**NOTE #2**: In c9, you are typing and pasting commands inside a blue tab (May differ in color depending on workspace's color theme) called the `bash`**,** or terminal to be specific  

![bash](https://raw.githubusercontent.com/yahiae6643/github-tutorial/master/bash.png)

1. Within the front page of github, press the button "New repository"
2. The page you are taken to will ask for a title for your new repository (_description optional_). Type in your prefered title and press "Create repository"
3. The repository will include two lines of git commands  

``` 
git remote add origin git@github.com:yahiae6643/FAKE-REPO.git
git push -u origin master
```
4. Create a workspace by pressing **Create a New Workspace.** Give it a name (description is optional) and choose **Blank** as its template
4. Access your c9 workspace and create a directory _(directory is another name for folder)_ 
    * To create a new directory, type in `mkdir * Any file name * ` *,* which would create a new directory within your current location (the working directory)
    * Go inside your new directory by typing `cd *Name of repository*`**,** which changes you from your old location to a new location of your choice (To the new directory)
    * To turn the directory into a folder that runs on _Git_, type in `git init`**.**
    * Finally, paste each command from the remote repository (the repository in github) into the c9 bash 
> Your local repository (the repository that is currently within your machine) is now linked to your remote repository, meaning you have the ability to send your changes from your local to your remote 

5. To start making a file and saving it to your local repository, type in `touch *file name*`**.** This creates a file with a name of your choice in your working directory 
6. Access your file by typing in `c9 *file name*`, which brings you to your file's text editor. Edit your file any way you like and type `git add *file name*`
    * You can also `git add` a file that is completely blank 
7. Finally, type in `git commit -m *message*`**.** This permanently saves the file within the directory into your local repository.
> The `-m` within the git command means message. The message is usually the word or sentence in front of `-m`, so it necessary to add a message in order for the command to  properly execute
8. Finally, type in `git push`**,** which sends your changes in your local repository to the remote repository it is linked to.
9. Go to your remote repository in github and see your files!

---
## Workflow & Commands
###### The workflow involves.. 
* _making changes to a file or deleting it in your directory_ 
* _temporarily saving the changes of your file_ 
* _permanently saving the changes as previous versions of the repository_
* _sending the changes from your local repository to your remote repository_

NOTE: Commands start with `git` since they are apart of git's system   
NOTE #2: Working directory means the directory you are currently located in

![Flowchart](https://raw.githubusercontent.com/yahiae6643/github-tutorial/master/flowchart.png)
`Image source: https://www.codecademy.com/ ("Learning Git")`

| Git Commands  | Format | Use | Pointers |
| --- | --- | --- | --- |
|  init | `git init`  | `git init: To initalize (or to start) git within your new or recently modified directory`| Without initalizing git in your directory, you won't have the ability to execute other git commands in order to save files within your local repository.|
| add  | `git add *file name*, *file name #2*, etc` | `Prepares one or more of your files' changes into the staging area for committing. It "stages" the files to the staging area`  | The **staging area** is a area where you temporary save your changes until they are ready to be permanantly saved as a previous version of the repository. |
|  add . |`git add *.*`| `Prepares all files into your staging area that are modified or new to be committed but rejects all files that are deleted` | **N/A** |
| add --all | `git add *--all*` | `Prepares all files into your staging area that are new, modified, AND deleted for being committed` | When a file is deleted, Git keeps track of the change. This change can be added into the staging area and be considered a previous version of your project when placed in your repository   |
|  diff | `git diff`  | `Displays the difference between your current file and the latest (HEAD) version of your file within the repository`| **N/A**|
|  status | `git status`  | `Shows which files are staged, not staged, and are not tracked by git `| "not tracked" means the files' changes aren't being monitored by git| 
| commit | `git commit -m *message*` | `Saves files from the staging area permanently into your repository as a previous version of the project. It "commits" a file into the local repository`| The most recent saved changes in your repository (or most recent commit) is called the `HEAD` commit. Also, the `-m` within the command assigns any text after it as a message for the new commit, which can help you distinguish and pinpoint your commits  |
|  log | `git log`  | `Shows all previous versions. Basically, the commits are located in the repository of your project`| These commits include messages you made, the time it was made, the name of who made it, and a 40 character code called a `SHA`. The `SHA` can be used to distinguish commits between each other, but can be also used in removing a commit or reverting back to a commit you desire. An example of a `SHA` is `5d1da5b98cecf7ec68e91bb923aa76d45f8e7807`|
| remote | `git remote add origin *URL*`  | `Establishes the connection between your local repository and your remote repository in Github`| `remote` refers to setting up the connection b/w your local repository and the repository within github (the remote repository). `add` refers to your remote repository and its commits. `origin` is a nickname for your remote repository. `url` means the url of your remote repository, the location of the remote repository (SHOULD BE SSH LINK) |
| push -u | `git push -u origin master` | `Transfers your local commits to the remote repository`| `push` means sending your commits from your local repository into your remote repository. `-u` means upstream. This will make the terminal remember to always send the local commits to a certain branch in your remote repository. `origin` refers back to the nickname of the remote repository. `master` refers to the branch in the remote repository that should contain your local commits|
|  push | `git push`  | `Just like "git push -u origin master," the command sends your local commits from your local repository to your remote repository in github. HOWEVER, it now has the knowledge on which branch in your remote repository to push the commits to`| This command is used soon after using `git push -u origin master`|  
| remote -v | `git remote -v`| `Displays the remote repository that you are send and taking commits  (The remote repository your local repository is connected to). It always shows the SSH link of your repository in github` | `-v` sends for verbose, which means to tell everything about a certain subject.|
| clone | `git clone *SSH Link*` | `Creates a copy of a repository on github inside your working directory` | The SSH link of the repository is always found when clicking the *Clone or download* and pressing _Use SSH_ on the top right of the box |

| Essential Command Line Add-Ons | Format | Use | 
| --- | --- | --- |
|`cd`|`cd *directory_name*`| `Moves you from one directory to another` |
|`pwd`|`pwd`| `Prints your current work path. e.g: Im located in yahiaelhag:~/workspace/github-tutorial` |
|`rm`|`rm *file_name*`| `Removes a file from a directory. The files usually have extensions like .txt or .png` |
|`rmdir`|`rmdir *directory_name*`| `Removes a empty directory (A folder with no content inside)` |
|`rm -rf`|`rm -rf *file_name or directory_name*`| `Removes a directory or file with force until the container and the content inside is fully deleted` |
|`mv (VERSION ONE)`|`mv *file_name or directory_name* *new file_name or new directory_name`| `Renames or Assigns a directory or file a new name of your choice` |
|`mv (VERSION TWO)`|`mv *file_name or directory_name* *EXISTING directory_name`| `Moves a directory or file into a existing directory (A folder that is in located within your work directory or parent directory (The folder that contains all other folders. THE PARENT IS NEVER ~)` |
|`touch`|`touch *file_name.extension*`| `Creates a new file with a name and extension (e.g: .txt, .png) of your choice. Extensions are optional.`|

**EXTRA TIPS TO FOLLOW:**  
* Never use `git init` in the root directory (`EXAMPLE_USERNAME:~ `)**.** This would cause many problems if you continue your workflow
    * To fix this problem, type in `rm -rf .git` within the root directory. This will remove the source folder that helps initalize _Git_ in the directory, which will uninitalize the directory from _Git_
* Use `git status` oftenly, since the command can be used freely without problem and it can help you choose which file changes are necessary to prepare for commiting
* Use `git remote -v` oftenly to check if your local repository is connected to the **correct** remote repository (The remote repository you want to connect to)



---
## Rolling Back Changes

| Github commands | Format | Use | Pointers |
| --- | --- | --- | --- |
| checkout | `git checkout *branch* *file_name*` | `Changes your files' content back to when it looked like the HEAD commit`| This is unclear, so here is an example. My `HEAD` commit was when my `hello.txt` file said "Hello Tim." However, I recently changed "Hello Tim" to "Hello Johnny" in my file and I want to change it back. So when I used `git checkout HEAD hello.txt`**,** it changed the file's content to when it looked like the 'HEAD' commit, which was "Hello Tim". This means that the command reverts your file back to its the latest saved change.  |
| reset HEAD | `git reset HEAD *file_name*` | It removes changes of a chosen file saved in your staging area| An example would be creating a file called `practice.txt` and typing a few things in its text editor. You decided to `git add practice.txt`**,** adding the changes you recently made to your file in the staging area and preparing it to be committed. However, you realize you want to change the file differently and add that change instead. This causes you to use `git reset HEAD practice.txt` and removing the recent file change you staged. You can now happily edit the file to your preference and add the change into the staging area, preparing it for a future commit. |
| reset soft | `git reset --soft HEAD~1` | `Reverts the HEAD commit by one previous commit. However, your files' content and prepared file changes within the staging area stays the SAME as before. It destroys the HEAD commit but doesn’t destroy its content and staged files.` | e.g: Your current `HEAD` commit that says "Dogs are better than cats." Your staging area is empty and your file says the same thing as the head commit. However, you decide to change the file to "Cats are better than dogs" and add it to the staging area. You later commit the change and that will become the HEAD commit. However, you want to change back to the previous commit so you use `git reset --soft HEAD~1`**.** Your previous commit is now the `HEAD` commit but the content still says "Cats are better than dogs." And, the file changes "Cats are better than dogs" are  staged within the staging area, just like the commit we destroyed. |
| reset hard | `git reset --hard HEAD~1` | `The HEAD commit is reverted back by one previous commit but the staging area's prepared files from before and as well as the files' content CHANGES back to when it looked like previous commit that you reverted to. Destroys the HEAD commit, its content, and its staged files (The staging area will be empty)` | You recently made a new file and added "10/10" into the file's text editor. You then stage the change in the staging area and commit it. However, you decide to change "10/10" to "5/10" in the file and do the process of adding and committing again for your recent change. You want your file, staging area, and commit to be back when they had "10/10" so you use `git reset --hard HEAD~1`**.** The `HEAD` commit and its file content and prepared files in the staging area are deleted, bring you back to the previous `HEAD` commit. You now have "10/10". |
| revert | `git revert *a / b / c / ...* *SHA*` | `Reverts your HEAD commit to a previous commit of your choice, which also changes the staging area and file content associated to the commit you reverted to` | `a`: refers to first previous commit, `b`: refers to the second previous commit, etc... (The previous SHA associated to the letter must be included) |
