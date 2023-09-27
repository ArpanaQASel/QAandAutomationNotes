
# GIT 

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_logo1.png" > 


### What is Version Control?

Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later. So ideally, we can place any file in the computer on version control.

### What is Git?

Git is a **version-control system** for tracking changes in computer files and coordinating work on those files among multiple people. Git is a Distributed Version Control System. 
Git helps you keep track of the changes you make to your code. It is basically the history tab for your code editor. If at any point while coding you hit a fatal error and don’t know what’s causing it you can always revert back to the stable state. So it is very helpful for debugging. Or you can simply see what changes you made to your code over time.

**What is a Repository?**

A repository a.k.a. repo is nothing but a collection of source code

***There are four fundamental elements in the Git Workflow:***

+ Working Directory
+ Staging Area
+ Local Repository 
+ Remote Repository.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/Git_Workflow.png" >

**If you consider a file in your Working Directory, it can be in three possible states.**

**Staged** - Which means the files with the updated changes are marked to be committed to the local repository but not yet committed.

**Modified** - Which means the files with the updated changes are not yet stored in the local repository.

**Committed** - Which means that the changes you made to your file are safely stored in the local repository.

### Commands

**1. git init**

Usage: 
```
git init [repository name]
```

We have to navigate to our project directory and type the command git init to initialize a Git repository for our local project folder. Git will create a hidden .git directory and use it for keeping its files organized in other subdirectories.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_init.PNG" >


**2. git add**

Usage (i): 
```
git add [file(s) name]
```

This will add the specified file(s) into the Git repository, the staging area, where they are already being tracked by Git and now ready to be committed.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_add1.png" >

Usage (ii): 
```
git add . or git add *
```

This will take all our files into the Git repository, i.e., into the staging area.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_add2.png" >

**3. git commit**

Usage: 

```
git commit -m “message”

```

This command records or snapshots files permanently in the version history. All the files, which are there in the directory right now, are being saved in the Git file system.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_commit.png" >

**4. git status**

Usage: git status

This command will show the modified status of an existing file and the file addition status of a new file, if any, that has to be committed.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_status.png" >

**5. git remote**

Usage: 

``` 
git remote add origin “[URL]” 
```

Once everything is ready on our local system, we can start pushing our code to the remote (central) repository of the project. For that, follow the below steps:

***Step 1:***

(1) Login to the **GitHub account** if the account already exists (If not, sign up on github.com)

(2) Click on **New**

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git.png" >

***Step 2:*** 

Now, we have to create a new repository. Provide a **name** to our **repository**, select the privacy of the repository as **Public**, and then click on **Create repository**.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_remote1.PNG" >

Once we are done with filling up the new repository form, we would land on a page as follows:

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_repo.PNG" >

**Step 3:**

Click on the Copy icon on the right side of the URL box of the Github repository to copy the link and paste it as shown below:


```
  git remote add origin “URL”
```
Now, we are ready to operate the remote commands in our repository that we have just created.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_remote_add.png" >

**6. git push**

Usage:
```
git push origin [branch name]
```


Suppose, we have made some changes in the file and want to push the changes to our remote repository on a particular branch. By using the command ‘git push,’ the local repository’s files can be synced with the remote repository on Github.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_push.png" >

**7. git clone** 

Usage: 
```
git clone [URL]
```

Suppose, we want to work on a file that is on a remote Github repository as another developer. How can we do that? We can work on this file by clicking on Clone or Download and copying the link and pasting it on the terminal with the git clone command. This will import the files of a project from the remote repository to our local system.

(1) The below screenshot shows from where to copy the link:

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_clone.png" >

To create a local folder, we have to use the following command:
```
mkdir [directory- name]
cd [directory- name]
git clone [URL]
```

Now, paste the copied link along with the git clone command as shown below:

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_clone1.png" >

> Note: Here, we don’t have to use the git remote add origin command because we have already cloned the remote repository in the local directory. Now, if we push any new file, it knows where it has to go.

**8. git branch**

Usage (i): 
```
git branch [name-of-the-branch]
```

When multiple developers are collaborating on a project or repository, branches become essential for managing different workspaces. Using this command, we can create a new branch (for example, ‘branch1’). This allows developers to work independently on their respective branches, making changes and commits without affecting the main branch or other branches.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_branch.png" >

Usage (ii): 
```
git branch -D [name-of-the-branch]
```

Likewise, to delete a branch, we utilize the “git branch -D” command. This enables us to remove a specific branch (e.g., ‘name-of-the-branch’) that is no longer needed, cleaning up the repository and reducing clutter.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_branch_d.png" >

**9.git diff**

Usage: 
```
git diff [commit-id-of-version-x] [commit-id-of-version-y]
```

Diffing is a function that takes two input datasets and outputs the changes between them. The git diff command is a multi-use Git command which, when executed, runs a diff function on Git data sources. These data sources can be commits, branches, files, and more. The git diff command is often used along with the git status and git log commands to analyze the current state of our Git repository. We use git log to get the details of commit IDs.

Let’s compare the working directory with the index as shown below:

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_diff.png" >

**10. git log**

Usage : 
```
git log
```

The “git log” command is handy when we want to examine the detailed log of every commit in our repository. By executing this command, we can view the log specific to the branch we are currently in. Additionally, we can use “git log -3” to display the last three logs.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_log.png" >

**11. git stash**

Usage: 
```
git stash
```

This command can be used when we want to save our work without staging or committing the code to our Git repository and want to switch between branches.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_stach.png" >

**12. git revert**

Usage: 
```
git revert [commit id]
```

The git revert command can be considered as an ‘undo’ command. However, it does not work as the traditional ‘undo’ operation. It figures out how to invert the changes introduced by the commit and appends a new commit with the resulting inverse content.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_revert.png">

**13. git merge**

Usage: 
```
git merge [another-file-name]
```

This command will combine multiple sequences of commits into one unified history. In the most frequent use cases, git merge is used to combine two branches. The git merge command takes two commit pointers, usually the branch tips, and finds a common base commit between them. Once it finds a common base commit, it will create a commit sequence.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_merge.png">

**14. git fetch**

Usage: 
```
git fetch
```

When we use the command git fetch, Git gathers any commit from the target branch that does not exist in our current branch and stores it in our local repository. However, it does not merge it with our current branch.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_fetch.png">

In situations where we want to keep our repository up to date but are concerned that updating our files might lead to issues, a specific technique comes to the rescue. To integrate the commits into our master branch, we use the merge feature. This feature actively retrieves all the branches from the repository and then proceeds to download all the required commits and files from another repository. It ensures that our repository remains current while mitigating the risk of potentially breaking our ongoing work.

**15. git pull**

Usage: 
```
git pull origin master
```

The git pull command first runs ‘git fetch’ which downloads the content from the specified remote repository and then immediately updates the local repo to match the content.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_pull.png">

### Upload a file in Git without Commands

After creating a repo, click on the **Add file** button. In that choose **Upload files**.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_drag.PNG">

Then, click on **choose your files** and select the file from you local system that needs to be added in repo. 

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_choose_file.PNG">

After choosing the file, click **commit changes**.

<img src="https://github.com/LeemaJosephine18/GitContents/blob/main/git_commit_changes.PNG" >

## Git Overview

+ **Version Control System (VCS):** Git is a distributed version control system designed to track changes in source code and facilitate collaboration among multiple developers.

+ **Repository:** A repository, often referred to as a "repo," is a central location where Git stores all the files, history, and metadata of a project.

+ **Commits:** A commit is a snapshot of changes made to the repository. It represents a logical unit of work and includes a unique identifier, a commit message describing the changes, and a reference to the previous commit.

+ **Branches:** Git allows for the creation of multiple branches, which are independent lines of development. Branches enable developers to work on separate features or bug fixes without interfering with the main codebase.

+ **Master/Main Branch:** The main branch, traditionally named "master" or "main," serves as the default branch and typically represents the stable version of the code.

+ **Checkout:** The act of switching to a different branch is called checkout. It allows developers to work on a specific branch and access its code and history.

+ **Merge:** Merging combines the changes from one branch into another. It integrates the commits of a source branch into a target branch, incorporating all the changes seamlessly.

+ **Pull/Pull Request:** When working collaboratively, a developer can request changes from their branch to be merged into another branch through a pull request. This process allows for review and discussion before the merge takes place.

+ **Push:** Pushing refers to sending local commits to a remote repository, updating it with the latest changes. This step makes the changes accessible to other developers working on the same repository.

+ **Remote Repository:** A remote repository is a copy of the repository stored on a server or hosting platform. It allows for collaboration and synchronization among multiple developers.

+ **Clone:** Cloning is the process of creating a local copy of a remote repository. Developers can clone repositories to their local machines to work on the code and contribute to the project.

+ **Fetch:** Fetching retrieves the latest changes from a remote repository without integrating them into the local codebase. It updates the local repository's knowledge of the remote repository's state.

+ **Pull:** Pulling combines the fetch operation with automatically merging the changes into the current branch. It allows developers to update their local codebase with the latest changes from a remote repository.

+ **Conflict Resolution:** Conflicts may arise when merging or pulling changes if two or more developers modify the same part of a file. Git provides tools to help resolve these conflicts manually by choosing which changes to keep.

+ **Staging:** Git uses a staging area (also called the "index") to prepare files for commit. Developers can selectively stage specific changes or files, controlling which modifications will be included in the next commit.

+ **Ignoring Files:** Git allows developers to specify files or patterns to ignore, ensuring that certain files, such as compiled binaries or sensitive information, are not tracked or committed.

+ **Tagging:** Tags provide a way to mark specific points in Git history, such as release versions or important milestones. They allow for quick reference to specific commits, providing a more user-friendly identifier.

+ **Git Workflow Models:** Git supports various workflow models, including centralized, feature branch, and Gitflow. These models define how developers collaborate and manage branches and merges within a project.

+ **Git GUIs and Clients:** While Git can be used through the command line interface (CLI), there are also graphical user interfaces (GUIs) and dedicated clients available that provide a more visual and user-friendly interaction with Git.

+ **Git Hosting Platforms:** Git repositories can be hosted on various platforms like GitHub, GitLab, and Bitbucket.