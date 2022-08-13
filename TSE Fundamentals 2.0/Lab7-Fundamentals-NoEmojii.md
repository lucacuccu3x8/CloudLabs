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
2. Attempt to **create two directories** in the `/var` directory, named `task7a` and `task7b`
3. Set the proper permissions to **allow** the user ‘sophos’ and all others to write in the `/var` directory
4. Write down the command(s) used to give sufficient permissions to the `/var` directory:

```csharp
Chmod 773 /var
```

 
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


> **e.g.,** You could you use one line command:

```csharp
echo -e “This content is from file1\nThis is line 2” > task7a/file1.log
```
> **Note:** `\n` Indicates to write in a new line.

7. Create a copy of `/var/task7a/file1.log` and save it to `/var/task7b` 
Then rename the `/var/task7b/file1.log` to `file1b.log`

> **e.g.,** You could you use one line command:

```csharp
/var#  cp task7a/file1.log task7b/ && mv task7b/file1.log task7b/file1b.log
```

8. Write down the command(s) used to copy the file;
9. Write down the command(s) used to rename the file;

10. Set the permissions of the file `‘file1b.log’` to the following parameters: 

```csharp
-rwxr-x--x 1 sophos staff 42 <timestamp> file1b.log
```

11. Write down the command(s) used to set the permissions of `file1b.log` 
 

##### ![check](JPG/pngegg%20(1).png) You have successfully created, copied, renamed, and modified file permissions. 





***

## **Task 7.2:** <small>Make Edits and searches using VI</small> 
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

## **Task 7.3:** <small>Search using various grep commands through system files </small> 


![![London ](JPG/London%20Client.png)](JPG/London%20Client.png)


 
 
 
##### ![check](JPG/pngegg%20(1).png) You have now successfully made various DNS request types and analyzed their packets. 


***

## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
1.	Displayed the routing table from a Windows and Linux Client  
2.	Configured a DHCP server and observed the various negotiations and behavior 
3.	Looked up and resolved several types of DNS records using nslookup 

***





