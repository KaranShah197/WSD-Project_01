# WSD-project1

## Basic commands to manage the file systems on Linux

The vi (visual) utility is a screen-oriented text editor. Following is the syntax for writing the vi command

    vi [−rR] [−c command] [−t tagstring] [−w size] [file...]

![vi example](/images/vi_open.PNG)
![vi editor](/images/vi_edit.PNG)
    
The following operations shall be supported by vi:

* -c `command`
        Specify an initial command to be executed in the first edit buffer loaded from an existing file.
* -r
    Recover the named files.
* -R
    Set `readonly` edit option.
* -t `tagstring`
    Edit the file containing the specified tagstring.
* -w `size` 
    Set the value of the `window` editor option to size.