# **Lab 5: Tools**

## Objectives
Upon successful completion of this lab, you will be able to: 
1.	Understand the uses of the **Process Monitor** Tool  
2.	Understand the uses of the **Process Explorer** Tool  
3.	Utilize **Wireshark** to capture and filter traffic 

### Lab Diagram:
![London DC](JPG/London%20DC%202.png)

***

## **Task 5.1:** Debug with Process Monitor Tool
You have been given a task where you need to capture all events i.e., Registry activity, File System activity, Network activity and Thread activity, while accessing a website from Google Chrome. 

#### Let's begin:
![](JPG/London%20DC%204.png)  

1. Open Process Monitor and start a capture
![procmon](JPG/procmon-app.png)


2. Open **Google Chrome** and browse any website
3. Filter for Google Chrome processes and all its **subtrees**.
4. Note down all the **PIDs** used by Google Chrome:
5. Save the filtered capture as a **PML** file  
 and write down all the distinct types of events:

##### ![check](JPG/pngegg%20(1).png) You have successfully debugged using the Process Monitor Tool


***

## **Task 5.2:** <small>Debug with Process Explorer</small> 
You have been asked to debug information using the command prompt with the help of the Process Explorer tool  


![](JPG/London%20DC%204.png)  
1. Open the **Process Explorer** and run Command Prompt 

2. Find the Command Prompt process and check all the information   
> **i.e.,** PID, Company Name, CPU, Memory Usage 


3. Review all the available options

> **Note:** These options include Kill Process, Create 
Dump, Virus Total check, Restart, Suspend, 
Properties and Verify Image Signatures 


4. Save the filtered capture for Command prompt in Process Explorer Data (.txt) format  

##### ![check](JPG/pngegg%20(1).png)  You have successfully performed a debug using Process Explorer 


***

## **Task 5.3:** <small>Wireshark Debugging</small> 

You have been asked to obtain the following information from a Wireshark capture: 

*	Wireshark Filter **by IP** 
*	Wireshark Filter **by Port**  
*	Wireshark Filter **by IP** and Port 
*	**Mac Address** Filter 
*	Filter **by URL** 
*	**Trace TCP Stream** for website communication 
*	**Filter out** Destination IP address


![](JPG/London%20DC%204.png)  


1. 	Open Wireshark start a **packet capture** and access any **HTTPs** based Website. 

![Wireshark](JPG/Wireshark.png)

2.	Note down and verify the commands used to filter for the information outlined in the task above. 
 
3. 	Save the capture in **PCAP format** after validating. 

##### ![check](JPG/pngegg%20(1).png) You have successfully utilized filters with Wireshark 


***

## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
1.	Debugged using Process Monitor Tool  
2.	Debugged using Process Explorer Tool  
3.	Wireshark Debugging 

***





