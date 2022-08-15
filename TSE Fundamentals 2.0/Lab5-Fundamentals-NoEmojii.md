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

1. Open **Process Monitor** and start a capture;   
use the shortcut in the Desktop: "**Procmon64**"
![procmon](JPG/procmon-app.png)


2. Open **Google Chrome** and browse any website
3. Go back to **Procmon64** and in the "Filter" tab on top, apply a filter for all "chrome.exe" processes and all its **subtrees**.

> **Note:**  You could also apply a similar filter by right-click "chrome.exe" in the list of all captured processes. ![](JPG/Procmon.png)

4. Once the filter is up, note down all the **PIDs** used by Google Chrome associates.
5. Save the filtered capture as a **PML** file  
 and write down all the distinct types of events.

##### ![check](JPG/pngegg%20(1).png) You have successfully debugged using the Process Monitor Tool


***

## **Task 5.2:** <small>Debug with Process Explorer</small> 
You have been asked to debug information using the command prompt with the help of the Process Explorer tool  


![](JPG/London%20DC%204.png)  
1. Open the **Process Explorer** using the shortcut from the Desktop.

![Process Explorer](JPG/Process%20Explorer.jpeg)

2. Open the Windows CMD prompt.

3. Back in the **Process Explorer**, now find the Command Prompt process, right click and select "**Properties**" to check all the information about **PID**, **Company Name**, **CPU**, **Memory Usage** 

![](JPG/ProcessExplorer2.png)


4. Review all the available options and tabs from the dialog box

> These options include:
> * Kill Process, 
> * Create Dump, 
> * Virus Total check (Brand New Feature!) 
> * Restart, Suspend a process
> * Verify Image Signatures 


5. Save the filtered capture for Command prompt in Process Explorer Data (**.txt**) **format** 

#### ![check](JPG/pngegg%20(1).png)  You have successfully performed a debug using Process Explorer 


***

## **Task 5.3:** <small>Wireshark Debugging</small> 

You have been asked to obtain information about active peers in the network from a Wireshark capture.


![London DC](JPG/London%20DC%204.png)
1. Open **Wireshark**, and start a packet capture from the "**Ethernet**" interface.

2. Now, open **Chrome or Firefox** and attempt to access any **HTTPs** based Website.
> **e.g.,** `https://www.sophos.com`

3. Go back to Wireshark and observe the packets being captured in the "**Packet List Pane**" as soon as they leave/enter the Ethernet interface.

![Wireshark](JPG/Wireshark.png)

4. Research and Note down the Display-Filters and the respective syntax to quickly highlight and extract the following information:
*	Wireshark Filter **by IP** 
*	Wireshark Filter **by Port**  
*	Wireshark Filter **by IP** and Port 
*	**Mac Address** Filter 
*	Filter **by URL** 
*	**Trace TCP Stream** for website communication 
*	**Filter out** Destination IP address
 >**Note:** You can find a useful cheat list of Display-Filters here:
 https://packetlife.net/media/library/13/Wireshark_Display_Filters.pdf
 
5. Save the capture in **PCAP format** after validating.


##### ![check](JPG/pngegg%20(1).png) You have successfully utilized filters with Wireshark 


***

## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
* Debugged using Process Monitor Tool
* Debugged using Process Explorer Tool
* Wireshark Debugging

***
***
### Before closing this page:
> Please remember to "Deallocate" the "HostVM" in the "Resource Tab" before closing this LAB, 
![](JPG/Deallocate%20the%20VM.png)
otherwise please continue to the next LAB.



