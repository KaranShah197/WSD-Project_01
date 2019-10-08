# WSD-project1

## **Explain how the usage of Git, Docker, automated testing, and continuous integration can improve the productivity and competitiveness of a company.**

Git, Docker, automated testing, and continuous integration all have a significant learning curve.
 
**Git** benefits every aspect of an organization, from the development team to the marketing team, and everything in between. It is an Open Source Distributed Version Control System. This basically means that Git is a content tracker and is used to store content — it is mostly used to store code due to the other features it provides. The code which is stored in Git keeps changing as more code is added. Also, many developers can add code in parallel. So Version Control System helps in handling this by maintaining a history of what changes have happened. Real life projects generally have multiple developers working in parallel. So a version control system like Git is needed to ensure there are no code conflicts between the developers. For more information visit [Git](https://www.atlassian.com/git/tutorials/why-git).

**Docker** is a platform that allows users to easily pack, distribute, and manage applications within containers. In other words, it is an open-source project that automates the deployment of applications inside software containers. Docker really makes it easier to create, deploy, and run applications by using containers, and containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package. By doing so, the developer can be assured that the application will run on any other Linux machine regardless of any customized settings that machine might have that could differ from the machine used for writing and testing the code. For more information visit [Docker](https://www.docker.com/why-docker).

**Automated testing** is the act of conducting specific tests via automation as opposed to conducting them manually. It is quickly becoming necessary for micro, small, and medium-sized enterprises (SMEs) to automate their testing processes. Test automation increases overall software efficiency and ensures robust software quality. There are specific tools that can effectively execute automated test cases, and help in comparing actual and expected results. In this manner, automated testing can guarantee software proficiency without involving repeated and manual intervention. One of the biggest business perks of automated testing is that it can be implemented time and again, with minimal effort and maximum accuracy. Read more about [Automated Testing](https://smartbear.com/solutions/automated-testing/).

**Continuous Integration** is used speed up and automate the software delivery lifecycle. It is a DevOps process that is integral to continuous delivery, has code committed into source control and builds automatically performed “continuously.” Continuously integrating code improves processes in a way that benefits both IT teams and their business counterparts. Continuous integration continuously processes, tests, and uploads changes or additions made to a code base. The code is saved in a source control management system that is accessible to all developers for testing and reference. Any developer working on the application has access to the most current code. Read more about [Continuous Integration](https://www.thoughtworks.com/continuous-integration).

## Basic commands to manage the file systems on Linux

The vi (visual) utility is a screen-oriented text editor. Following is the syntax for writing the vi command

    vi [−rR] [−c command] [−t tagstring] [−w size] [file...]

![vi example](/images/vi_open.PNG)
![vi editor](/images/vi_edit.PNG)
    
    The following operations shall be supported by vi:
   * -c `command`      : Specify an initial command to be executed in the first edit buffer loaded from an existing file.
   * -r                : Recover the named files.
   * -R                : Set `readonly` edit option.
   * -t `tagstring`    : Edit the file containing the specified tagstring.
   * -w `size`         : Set the value of the `window` editor option to size.


* **CD Command**  
    cd - change the working directory.  
    This command will allow you to change the working directories through terminal. Using cd we can change the working directory to any directory on machine.
    We can provide the relative path or absolute path to the same.  
    eg: cd /images/ - It will change the current working directory to /images.  
![cd example](/images/cd_command.PNG)

    The above was the example of relative path where we specified the the location of directory which was inside the current directory. Below is the example to change the working directory using relative path.  
    eg: cd /dev/home/usr/karan/project/

    We can also use .. to move to the parent directory  
    eg: cd ..  
    More details can be found at (http://man7.org/linux/man-pages/man1/cd.1p.html).  

* **mkdir Command**  
    mkdir - It will allow you to create new directory(s) (Make directory). It has the following syntax:  
    `mkdir [option] directory_name(s)`  
    Example: `mkdir music` it will create a diectory called music.
![mkdir example](/images/mkdir_command.PNG)
    
    We can also specify the multiple directory names.  
Example: `mkdir music video photo`

* **cp command**  
    cp - copy files and direcories.  
    Copy SOURCE to DEST, or multiple SOURCE(s) to DEST.  
    Example: `cp [OPTION]... SOURCE... DIRECTORY`
![cp example](/images/cp_command.PNG)

    We can pass following options to CP command
    * --backup[=CONTROL]  
        make a backup of each destination file
    * --copy-contents  
        copy contents of special files when recursive
    * -f, --force  
        if an existing destination file cannot be opened, remove it and try again
    * -i, --interactive  
        prompt before overwrite
    
    We can pass many more agruments to copy command. Please [click here](http://man7.org/linux/man-pages/man1/cp.1.html) to view the same.

* **pwd command**  
    pwd - It prints the name of current working directory. It can be written as follow:  
    `pwd [OPTION]...`  

    Example: pwd  
    Following options can be passed to the pwd command:  
    * -P, --physical  
        avoid all symlinks
    * --help  
        display this help and exit
    * --version  
        output version information and exit  

* **mv command**  
    mv - It is used to move or rename files. It can be written as follow:  
    `mv [OPTION]... SOURCE... DIRECTORY`
Example: `cp [OPTION]... SOURCE... DIRECTORY`
![ example](/images/mv_command.PNG)

    It will move the README_BACKUP.md file to the /music directory. We can compare it with CP command. The only difference is instead of copying into new Destination it moves to the new Destination. Following optional arguments can be passed:  
    * -f, --force  
        do not prompt before overwriting
    * -i, --interactive  
        prompt before overwrite
    * -n, --no-clobber  
        do not overwrite an existing file

    If you specify more than one of -i, -f, -n, only the final one takes effect.  
    To view entire list of arguments [click here](http://man7.org/linux/man-pages/man1/mv.1.html).

* **rm command**  
    rm - It will remove the file(s) or directory(s). rm removes each specified file. By default, it does not remove directories. We need to use --recursive (or -r or -R).    
    `rm [OPTION]... [FILE]...`  

    Example: rm -R music/  
    It will remove the music directory and all the directories and files inside it recursively.
![rm example](/images/rm_command.PNG)

    Arguments supported by rm command:  
    * -f, --force  
        ignore nonexistent files and arguments, never prompt
    * -i  
        prompt before every removal
    * -r, -R, --recursive  
        remove directories and their contents recursively
    * -d, --dir  
        remove empty directories
    
    To know more about rm command, please refer [this](https://linux.die.net/man/1/rm) link.

* **history command**  
    history - A GNU History Library. Many programs read input from the user a line at a time.  The GNU History library is able to keep track of those lines, associate arbitrary data with each line, and utilize information from previous lines in composing new ones.  

    Use the up and down key's to scroll through previously typed commands. Press [Enter] to execute them or use the left and right arrow keys to edit the command first.   
    The history command can be used to list Bash's log of the commands you have typed. This log is called the “history”. To access it type: `history n`  

    Example: `history 15`

    This will only list the last n commands. Type “history” (without options) to see the the entire history list.  
    References: http://man7.org/linux/man-pages/man3/history.3.html, https://linux.die.net/Linux-CLI/x1712.htm  

* **Home directory and ~**
    1. **Home directory**
        A `home directory` also called a `login directory` is a file system directory on Unix-like operating systems that serves as the repository containing a personal  files, directories and programs for a given user of the system. It is also the directory that a user is first in after logging into the system.  

        A home directory is created automatically for every ordinary user in the directory called `/home`,  standard subdirectory of the `root directory`.  

        A user with a user name of `tester` would typically have a home directory named `tester`. It would have an absolute pathname of `/home/tester`.  

        We can use `cd` command without any option to go to the user home directory.
    
    1. **Tilde (~)**  
        The `tilde` (`~` - the wavy horizontal line character) is used to represent users' home directories on Unix-like operating systems.  
        A user could also return to its home directory by using the tilde as an argument to cd, i.e.,  
            `cd ~`  
        The ~user shorthand variable refers to a user's home directory.(allowing the user to navigate to it from anywhere else in the filesystem, or use it in other Unix commands).  

More information can be found at http://www.linfo.org/home_directory.html


## **GitFlow Workflow**

GitFlow is branching model for Git. It is ideally suited for projects that have a scheduled release cycle. A Git flow consists of several steps including: 
* *Create a branch*
* *Add commits*
* *Open a pull request*
* *Review code*
* *Merge the code*
* *Deploy code*

![GitFlow Image](/images/GitFlow.PNG)

## **Terminology**

**Repository** is a git project. It contains all of the project's files and stores each file's revision history.

**Clone** is used to target an existing repository and create a copy of the target repository. When you create a repository on GitHub, it exists as a remote repository. You can clone your repository to create a local copy on your computer and sync between the two locations. 

**Fork** is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project. Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea.

**Branch** is a separate copy of the project that can be merged together. A branch is used to isolate development work without affecting other branches in the repository. Each repository has one default branch, and can have multiple other branches. You can merge a branch into another branch using a pull request.

**Commit** is a change. It is a difference between the previous and new version. It is a change to one or more files in your branch. Git assigns each commit a unique ID, called a SHA or hash that:
* tracks the specific changes
* when the changes were made
* created the changes

**Merge** is to put two branches (two version) together. It is used to merge a pull request into the upstream branch when work is completed. Anyone with push access to the repository can complete the merge.

**Checkout** is used to navigate between branches created by git branch. Checking out a branch updates the files in the working directory to match the version stored in that branch and it tells Git to record all new commits on that branch.

**Push** is used to upload local repository content to a remote repository. The git push command takes two arguments:
- a remote name, for example, origin 
- a branch name, for example, master

**Pull** is used to fetch and download content from a remote repository and immediately update the local repository to match that content. A pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.

**Remote Add / Remove / Show**

1. *Remote Add* adds a new remote in the directory the repository is stored at. 
1. *Remote Remove* removes a remote URL from the repository. 
1. *Remote Show* shows the shortnames of each remote handle you’ve specified.

**Status** displays the state of the working directory and the staging area. It lets you know if your commits meet the conditions set for the repository you're contributing to.

**Master Branch** is the default branch in Git. It is the one where all changes eventually get merged back into.