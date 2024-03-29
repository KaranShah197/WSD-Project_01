Git, Docker, automated testing, and continuous integration all have a significant learning curve.
 
**Git** benefits every aspect of an organization, from the development team to the marketing team, and everything in between. It is an `Open Source Distributed Version Control System`. This basically means that Git is a content tracker and is used to store content — it is mostly used to store code due to the other features it provides. The code which is stored in Git keeps changing as more code is added. Also, many developers can add code in parallel. So Version Control System helps in handling this by maintaining a history of what changes have happened. Real life projects generally have multiple developers working in parallel. So a version control system like Git is needed to ensure there are no code conflicts between the developers. For more information visit [Git](https://www.atlassian.com/git/tutorials/why-git).

**Docker** is a platform that allows users to easily pack, distribute, and manage applications within containers. In other words, it is an `open-source project` that automates the deployment of applications inside software containers. Docker really makes it easier to create, deploy, and run applications by using containers, and containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package. By doing so, the developer can be assured that the application will run on any other Linux machine regardless of any customized settings that machine might have that could differ from the machine used for writing and testing the code. For more information visit [Docker](https://www.docker.com/why-docker).

**Automated testing** is the act of conducting specific tests via automation as opposed to conducting them manually. It is quickly becoming necessary for micro, small, and medium-sized enterprises (SMEs) to automate their testing processes. Test automation `increases overall software efficiency and ensures robust software quality`. There are specific tools that can effectively execute automated test cases, and help in comparing actual and expected results. In this manner, automated testing can guarantee software proficiency without involving repeated and manual intervention. One of the biggest business perks of automated testing is that it can be implemented time and again, with minimal effort and maximum accuracy. Read more about [Automated Testing](https://smartbear.com/solutions/automated-testing/).

**Continuous Integration** is used speed up and automate the software delivery lifecycle. It is a `DevOps process` that is integral to continuous delivery, has code committed into source control and builds automatically performed “continuously.” Continuously integrating code improves processes in a way that benefits both IT teams and their business counterparts. Continuous integration continuously processes, tests, and uploads changes or additions made to a code base. The code is saved in a source control management system that is accessible to all developers for testing and reference. Any developer working on the application has access to the most current code. Read more about [Continuous Integration](https://www.thoughtworks.com/continuous-integration).


## **GitFlow Workflow**

GitFlow is branching model for Git. It is ideally suited for projects that have a scheduled release cycle. A Git flow consists of several steps including: 
* *Create a branch*
* *Add commits*
* *Open a pull request*
* *Review code*
* *Merge the code*
* *Deploy code*


### GitFlow Workflow Example
![GitFlow Image](/images/gitflow_workflow.png)

## **Terminology**

**Repository** is a git project. It contains all of the project's files and stores each file's revision history.

**Clone** is used to target an existing repository and create a copy of the target repository. When you create a repository on GitHub, it exists as a remote repository. You can clone your repository to create a local copy on your computer and sync between the two locations. 

**Clone Example**  
![Clone Image](/images/clone_example.JPG)

**Fork** is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project. Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea.

**Branch** is a separate copy of the project that can be merged together. A branch is used to isolate development work without affecting other branches in the repository. Each repository has one default branch, and can have multiple other branches. You can merge a branch into another branch using a pull request.

**Commit** is a change. It is a difference between the previous and new version. It is a change to one or more files in your branch. Git assigns each commit a unique ID, called a SHA or hash that:
* tracks the specific changes
* when the changes were made
* created the changes

**Commit Example**  
![Commit Image](/images/commit_example.JPG)

**Merge** is to put two branches (two version) together. It is used to merge a pull request into the upstream branch when work is completed. Anyone with push access to the repository can complete the merge.

**Checkout** is used to navigate between branches created by git branch. Checking out a branch updates the files in the working directory to match the version stored in that branch and it tells Git to record all new commits on that branch.

**Checkout Example**  
![Checkout Image](/images/checkout_example.JPG)

**Push** is used to upload local repository content to a remote repository. The git push command takes two arguments:
- a remote name, for example, origin 
- a branch name, for example, master

**Pull** is used to fetch and download content from a remote repository and immediately update the local repository to match that content. A pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.

**Pull Example**  
![Pull Image](/images/pull_example.JPG)

**Remote Add / Remove / Show**

1. *Remote Add* adds a new remote in the directory the repository is stored at. 
1. *Remote Remove* removes a remote URL from the repository. 
1. *Remote Show* shows the shortnames of each remote handle you’ve specified.

**Status** displays the state of the working directory and the staging area. It lets you know if your commits meet the conditions set for the repository you're contributing to.

**Master Branch** is the default branch in Git. It is the one where all changes eventually get merged back into.