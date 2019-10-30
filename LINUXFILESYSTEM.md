## Basic commands to manage the file systems on Linux

The vi (visual) utility is a screen-oriented text editor. Following is the syntax for writing the vi command

    vi [−rR] [−c command] [−t tagstring] [−w size] [file...]

![vi example](/images/vi_open.PNG)
![vi editor](/images/vi_edit.PNG)
    
* The following operations shall be supported by vi:
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
![mv example](/images/mv_command.PNG)

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
    history - A GNU History Library. Many programs read input from the user a line at a time. The GNU History library is able to keep track of those lines, associate arbitrary data with each line, and utilize information from previous lines in composing new ones.  
   
    The history command can be used to list Bash's log of the commands you have typed. This log is called the “history”. To access it type: `history n`  s

    Example: `history 15`

    This will only list the last n commands. Type “history” (without options) to see the the entire history list.  
    References: http://man7.org/linux/man-pages/man3/history.3.html, https://linux.die.net/Linux-CLI/x1712.htm  

* **home directory and tilde**
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

* **file paths in linux**  
    A file path is the human-readable representation of a file or folder’s location on a computer system. All files on linux machine's drive are in the system’s base (root) directory. Even external drives are brought into this root directory.  

    Files and folders on Linux are given names containing the usual components like the letters, numbers, and other characters on a keyboard. A path is a unique location to a file or a folder in a file system of an OS. A path to a file is a combination of / and alpha-numeric characters. That’s why you often see files listed in the format `/usr/bin/python3` or `/etc/os-release`. The forward slashes indicate that one item is stored inside of the item preceding it.  

    There are two types of filepaths in Linux System, Absolute path and relative path.  
    1. **Absolute paths**  
        An absolute path is defined as the specifying the location of a file or directory from the root directory(/). To write an absolute path-name:
        * Start at the root directory ( / ) and work down.
        * Write a slash ( / ) after every directory name (last one is optional)
        Example:  `vi /home/kvs32/abc.sql`  
        Even if file is in same directory we have written absolute path to access it.
    
    1. **Relative paths**
        Relative path is defined as the path related to the present working directly(pwd). It starts at your current directory and never starts with a `/` .  

        UNIX offers a shortcut in the relative pathname– that uses either the current or parent directory as reference and specifies the path relative to it. A relative path-name uses one of these cryptic symbols:  

        `.(a single dot) - this represents the current directory.`  
        `..(two dots) - this represents the parent directory.`  
        Example:   
            `Changing the directory with relatvie path:  cd music`  

    More information can be found at: https://opensource.com/article/19/8/understanding-file-paths-linux  

* **Using the tab key to complete file paths**  
    Tab completion is an extremely helpful feature in the Bash shell on Linux, or a terminal window on Mac OS X. Tab completion is an essential trick. It’s a great time saver and it’s also useful if you’re not sure of a file or command’s exact name.  

    For example, lets say, I want to move inside the images directory then I can just type `cd im` followed by the TAB key press. It will automatically complete the path.  
    However, if there are 2 or more folders with matching letters that we have types then on press of touble TAB key it will give you all matching folder names.  

    Example: `cd grails followed by double TAB key press`
    ![tab example](/images/tabkey.PNG)

* **Using up and down arrow for history**  
    As we have seen in the history command above, we can see the history of commands that we have typed so far using the history command and optionally typing the number of commands that we want to see.  
    There is another way to go back to history commands using the UP Arrow and the DOWN Arrow. In the terminal we can use the UP or DOWN arrows to navigate to the previous commands or next commands.

    Use the up and down key's to scroll through previously typed commands. Press [Enter] to execute them or use the left and right arrow keys to edit the command first.  