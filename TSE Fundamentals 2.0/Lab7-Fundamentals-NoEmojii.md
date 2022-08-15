# **Lab 7: Linux**

## Objectives
Upon successful completion of this lab, you will be able to: 
* Create, copy, move, and rename files
* Manage file and folder permissions
* Make edits to files using the text editor vi
* Search through files using the text editor vi
* Search through system files using various grep commands




### Lab Diagram:
![Lab7 Diagram](JPG/Lab6%20Diagram.png)

***

## **Task 7.1:** Create, copy and rename a file before managing permissions
You have been given a task to create two separate directories with two identical files. However, one file, ‘file1b.log’ requires different permissions than the original file. The ‘file1b.log’ requires file owner full permissions, the ‘games’ group read and execute permissions, and all others execute permissions only.  

#### Let's begin:
![London Client](JPG/London%20Client.png)
1. Open **PuTTY** and SSH to the **‘Linux Client’**: `172.17.17.22`   
as the user `sophos` and password: `Sophos1985` 

2. Attempt to **create two directories** in the `/var` directory, named `task7a` and `task7b`.
You will receive an error ‘**Permission denied**’.

3. Set the proper permissions to **allow** the user ‘sophos’ and all others to write in the `/var` directory
4. Write down the command(s) used to give sufficient permissions to the `/var` directory:

```csharp
Chmod 773 /var
```
>**Note:** You must login as the file owner or root user to modify the permissions of a file or directory. Password for root, is **Sophos1985**

 
5. Attempt to create the **two directories** in `/var` directory again 

```csharp
/var# mkdir task7a task7b
```

6. As the user ‘sophos’, **create a file** in `/var/task7a/` named: `‘file1.log’`  
with the following content: 

```csharp
This content is from file1   
This is line 2
```
Try to perform this step as efficient as possible

> **e.g.,** You could you use one line command:

```csharp
echo -e “This content is from file1\nThis is line 2” > task7a/file1.log
```
> **Note:** `\n` Indicates to write in a new line.

7. Create a copy of `/var/task7a/file1.log` and save it to `/var/task7b` 
Then rename the `/var/task7b/file1.log` to `file1b.log`

> **e.g.,** In the `/var directory`, You could you use one line command:

```csharp
cp task7a/file1.log task7b/ && mv task7b/file1.log task7b/file1b.log
```

8. Write down the command(s) used to copy the file;
9. Write down the command(s) used to rename the file;

10. Set the permissions of the file `‘file1b.log’` to the following parameters: 

```csharp
-rwxr-x--x 1 sophos staff 42 <timestamp> file1b.log
```
>**Note:** To modify the file you must be the file owner or group owner. 

11. Write down the command(s) used to set the permissions of `file1b.log` 
 

##### ![check](JPG/pngegg%20(1).png) You have successfully created, copied, renamed, and modified file permissions. 


***

## **Task 7.2:** <small>Make Edits and searches using **`vi`**</small> 
You have been given a task where the administrator requires you to add additional lines to the file `‘/var/file1b.log’` to diagnose an issue.   
It was suggested to use vi as there is no GUI on the Linux machine.   
Once complete, you must then search the file using a string and make a final line edit.  


![London Client](JPG/London%20Client.png) 
1. Append the following lines to the bottom of ‘/var/file1b.log’ using vi and save the file: 

```csharp
This is Line 3 
 This is LINE 4 This 
 is line 5
```
>**Note:**Case sensitivity is important in Linux. 

2. While still in vi, enter in the `‘/’` to run a search within the file. Enter in `/line` and hit enter to search. 
Press `‘n’` to jump between the search hits. 
Observe and take note of the cursor position. 

3. Write down why the **search/cursor** only jumps to line 2 and line 5 but none of the others: 

![](JPG/output-onlinepngtools.png) The reason is because the search is case sensitive – only line with exact string match will be shown by the search.
 
 
 
4. Edit line 1 using **vi editor** and change the first line to: 

```csharp
This content is from file1b.log
```

 
5. Write the changes and quit vi editor. Confirm the changes were successfully made have been saved. 

##### ![check](JPG/pngegg%20(1).png) You have successfully appended lines, searched, and made file content updates using vi. 

***

## **Task 7.3:** <small>Search using various **`grep`** commands through system files </small> 
You have been asked to gather all system logs for an event on January 22nd. The issue was reported at 7:15 AM but to ensure all the relevant logs are collected, you were tasked to gather everything that occurred on between 0700 and 0759. Understanding that it is your first-time searching content, your manager has provided you with a series of grep commands for practice. 

![![London ](JPG/London%20Client.png)](JPG/London%20Client.png)


1. Change directory to `/var/task7b` 
2. Run the following commands and take note of the different output from each: 
 
```csharp
grep ‘line 4’ file1b.log
```
> **Output:** None, grep is case sensitive!	
 	
```csharp
grep -i ‘line 4’ file1b.log
```

> **Output:** `-i` tells grep to skip case sensitive search in arguments

```csharp
grep -v file1b.log
```

> **Output:** the search for everything else excluding the matching argument. case/string

```csharp
grep -e ‘Line’ -e ‘LINE’ file1b.log
```


> **Output:** Show multiple matching searches in one command.	
 
	
4. Run a search to find all the syslog messages that occurred on **January 22nd on the 7th hour**.   
Send this output to the file `‘/var/task7a/syslogJan22.log’`

> **Note:** Confirm this file only contains syslog messages between 7 AM to 8 AM on Jan 22nd. 

5. Write down what command(s) were used to accomplish step 54: 

> ![](JPG/output-onlinepngtools.png)  Since there’s no `/var/log/syslog` and `/var/log/messages` storing all global system, the **output is clearly blank**!

**e.g.,** 
```csharp
Grep “Jan 22 07:[0-5][0-9]:[0-5] [0-9] > /var/task7a/syslog
```
‌‌ 

##### ![check](JPG/pngegg%20(1).png) You have now successfully searched files using grep and saved search results to a file. 

***

## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
1.	Created, copied, moved, and renamed files 
2.	Managed file and folder permissions 
3.	Made edits to files using text editor vi 
4.	Searched through files using text editor vi 
5.	Searched through system files using various grep commands 

***
‌‌ 

### Before closing this page:
> Please remember to "Deallocate" the "HostVM" in the "Resource Tab" before closing this LAB, 
![](JPG/Deallocate%20the%20VM.png)
otherwise please continue to the next LAB.



