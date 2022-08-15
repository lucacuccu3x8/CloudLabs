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

1. Open the PowerShell terminal and find the command to verify: **Network Statistics**   
> **i.e.,** 
> * Ethernet Name, 
> * Sent / Received Bytes, 
> * Received / Sent Unicast Packets.

A good cmdlet to start with is:
```powershell
Get-NetIpConfiguration
```

2. Write down all the cmdlets you found and the returned output for the recorded ‘**Network Statistics**’:

3. Research and list a few examples using the **Measure-Object** command.  
> **e.g.,** you can start your search from the PowerShell terminal, type:
```powershell
Get-Help Measure-Object
```
 
4. Write down the command **to verify** the status of the service, **‘ssh-agent’**:

> **Hint:** you could use `Out-String -stream | Select-String`   

5. Find out the command to verify **which process** is consuming **High CPU**.
 

##### ![check](JPG/pngegg%20(1).png)  You have researched and used various PowerShell commands

***

## **Task 4.2:** <small>Troubleshoot PowerShell Script not executing </small> 
A customer has created a test script ‘`Script.ps1`’ and wants to validate it by executing it before running the actual debug. However, when the customer tries to executes the script they are getting an error. Verify why the customer is not able to execute the script. 

#### Access the **London Client Virtual** Machine:

1. Within the "**Remote Desktop Connection Manager**" window, move your pointer to the left corner of your screen and from the pop-up menu, select the "02 - London Client"
2. A Dialog box will appear:
![](JPG/Dialog%20Login%20Box.png)

3. Enter the following credentials: 

|       |          |
|-------|----------|
| User: `SOPHOS\jsmith` | Password: `Sophos1985` |

4. Accept the certificate warnings and proceed further.
> **Note:** *Skip Step1 if you are accessing the London Client using the Hyper-V console.*

![](JPG/London%20Client.png)
 
5. Open the File Explorer and navigate into the `C:\` folder.
6. Double click the **script.ps1** file
> You should see nothing happening.

7. Open a **PowerShell terminal** and execute the script by running the command:  

```powershell
& “C:\Script.ps1”
```
 
 
 >![](JPG/output-onlinepngtools.png) **Note**: PowerShell scripts are stored as **.ps1** files. By default, you cannot run a script by just double-clicking the file or by simply invoking the execution from the PowerShell terminal. This protects your system from accidentally executing malicious scripts. 
 
8. Write down the error displayed after executing the script
 
 
9. Write down how you resolved the issue 

#### ![check](JPG/pngegg%20(1).png)  You have resolved an issue where PowerShell Scripts were not executing 

***

## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
1.	Performed basic troubleshooting using PowerShell 
2.	Troubleshot a PowerShell Script that was not executing 

***
***

> Please remember to "Deallocate" the "HostVM" in the "Resource Tab" before closing this LAB, 
![](JPG/Deallocate%20the%20VM.png)
otherwise please continue to the next LAB.



