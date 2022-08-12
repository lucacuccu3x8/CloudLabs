# **Lab 4: PowerShell**

## Objectives
Upon successful completion of this lab, you will be able to: 
1.	Perform basic troubleshooting using PowerShell 
2.	Troubleshoot an inoperable PowerShell script 



### Lab Diagram:
![London DC](JPG/London%20DC%202.png)

***

## **Task 4.1:** Basic Troubleshooting using Powershell

A customer wants to perform the following tasks with the help of PowerShell: 
 
*	List out statistics for the Network Connection 
*	Determine what commands are available for the Measure-Object command 
*	Verify the status of the ‘ssh-agent’ service  
*	List out the process which is consuming High CPU 

  
![](JPG/London%20DC%204.png)  

1. Open PowerShell and find the command to verify:**Network Statistics**   
>**i.e.,** Ethernet Name, Received Bytes, Received Unicast Packets, Sent Bytes, Sent Unicast Packets.

2. **Write down the command** and the returned output for the recorded ‘Network Statistics’:

3. Research and list a few examples using the **Measure-Object** command:
 
4. Write down the command **to verify** the status of the service, **‘ssh-agent’**:

5. Find out the command to verify **which process** is consuming **High CPU**:
 

##### ![check](JPG/pngegg%20(1).png)  You have researched and used various PowerShell commands

***

## **Task 4.2:** <small>Troubleshoot PowerShell Script not executing </small> 
A customer has created test script ‘Script.ps1’ and wants to validate it by executing it before running the actual debug. However, when the customer executes ‘Script.ps1’, they are getting an error. Verify why the customer is not able to execute the script. 

![](JPG/London%20DC%204.png)  
1. Open PowerShell and execute the script by running the command:  
 ```bash   
& “C:\Script.ps1”
```
 
 >**Note** PowerShell scripts are stored as .ps1 files. By default, you cannot run a script by just double-clicking a file. This protects your system from accidentally executing malicious scripts. 
 
 
2. Write down the error displayed after executing the script
 
 
3. Write down how you resolved the issue 
 
 
 
##### ![check](JPG/pngegg%20(1).png)  You have resolved an issue where PowerShell Scripts were not executing 

***

## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
1.	Performed basic troubleshooting using PowerShell 
2.	Troubleshot a PowerShell Script that was not executing 





