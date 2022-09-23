# **Lab 5: Tools**

## Objectives
Upon successful completion of this lab, you will be able to: 
1.	Understand the uses of the **Process Monitor** Tool  
3.	Utilize **Wireshark** to capture and filter traffic 
4.	Utilize **TCPDUMP** to capture and filter traffic from the command line

### Lab Diagram:
![](JPG/Diagram2.png)


***

## **Task 5.1:** Debugging process ID's with Process Monitor Tool

You have been given a task where you need to capture all events i.e., Registry activity, File System activity, Network activity and Thread activity, while accessing a website from Google Chrome. 

#### 
![](JPG/London%20DC%204.png)  

1. Double click and open "Procmon64" from the desktop.

![procmon](JPG/procmon-app.png)

2. Open and browse https://www.sophos.com using Google Chrome.

3. On Procmon64 application click on the "Filter" tab on top, apply a filter for all "chrome.exe" processes and all its subtrees.

> **Note:**  You could also apply a similar filter by right-click "chrome.exe" in the list of all captured processes. ![](JPG/Procmon.png)

4. Note down all the PID's used by Google Chrome. 

5. Click on File and Save the filtered capture as a PML file.

##### ![check](JPG/pngegg%20(1).png) You have successfully debugged using the Process Monitor Tool


***


## **Task 5.2:** Debugging Network activities using Wireshark tool. 

You have been asked to obtain information about active peers in the network from a Wireshark capture.  
Start practicing using the advanced **Wireshark Display-Filters** to quickly analyze and extract valuable information about network traffic.


![London DC](JPG/London%20DC%204.png)

1. Double click and open "Wireshark" tool from the desktop and start a packet capture from the "Ethernet" interface.

![](JPG/Ethernet.jpg)

2. Open and browse **https://www.sophos.com** using Google Chrome.

3. Back on the Wireshark application, we can observe the packets being captured in the "**Packet List Pane**" .

![Wireshark](JPG/Wireshark.png)

4. Research and Note down the **Display-Filters** and the respective syntax to quickly highlight and extract the following information:
*	Wireshark Filter **by IP** 
*	Wireshark Filter **by Port**  
*	Wireshark Filter **by IP** and Port 
*	**Mac Address** Filter 
*	Filter **by URL** 
*	**Trace TCP Stream** for website communication 
*	**Filter out** Destination IP address

>**Note:** You can find a useful **cheat list** of Display-Filters here:
> https://packetlife.net/media/library/13/Wireshark_Display_Filters.pdf
 
5. Save the capture in **PCAP format** after validating.


#### ![check](JPG/pngegg%20(1).png) You have successfully utilized filters with Wireshark 


***
## **Task 5.3:** Image Capture and Extraction using wireshark

Through traffic capture, Wireshark can be used to view and record all information during transit,
if this data is unencrypted such as images flowing to a device, Wireshark will record them and save the traffic information which can be extracted into Jpeg formats to be later collected for forensic evidences.  
In this task, We will browse the internet to an HTTP site while capturing the traffic with Wireshark. We'll then review the captured packets and extract the images which were sent from the website to the London-Client.

>**Note:** Note: In this exercise, you will access external websites, as these websites are
outside of our control, they are subject to change. If you do notice anything is out
of date, please let us know via our support desk so we can implement an update.

![](JPG/London%20Client.png)

1. Double click and open "Wireshark" tool from the desktop and start a packet capture from the "Ethernet" interface.

2. Open ans browse http://zero.webappsecurity.com using Google Chrome or Firefox browser.


![](JPG/ZeroBanking.png)

>**Note:** It is important to access an HTTP site as the information is transmitted in plaintext.

3. Allow **Chrome** to load all the pictures and content. Browse through the website for sometime.

4. On wireshark application click on the **Stop** Option below File TAB at the top.

![](JPG/zero2.png)

5. We know that the IP address of the **London-Client** is **172.17.17.20**, scrolling through the capture we will see the IP addresses listed on the capture. 

6. Find the "Apply a display filter bar" on top of the tool. Enter the Display-Filter as "HTTP" and hit enter.

![](JPG/zero3.png)

> **Note:** Initially when looking at the capture, we have a lot of information. But we know we were using HTTP traffic. Therefore, within the filter we are presented with only traffic on this protocol now.The majority of which comes from the IP address 172.17.17.20, as this was the main machine accessing the internet.

7. Right-Click on a **source address** of **172.17.17.20** and click on  "Follow > HTTP stream".

8. Type the following into the **Find field:** **jpg** Press Enter to find image details.

![](JPG/zero4.png)

9. We can see many jpeg files on the webpage and we have captured all those which were viewing in the webpage with Chrome.

![](JPG/find.png)

10. Use the "Find Next" button to locate the carousel_2.jpg.

11. Now close the "Follow HTTP Stream" box and on Wireshark application click on File > Export Objects> HTTP.

12. Click "Save All" option and save the content to Documents Folder.

![](JPG/carousel.png)

> **Note:** You can use the "**Find Next**" button to see the `carousel_2.jpg`

13. Open File Manager -> Documents folder.

![](JPG/filebox.png)

14. Here you can see all the objects and jpeg files from that http stream of packets, including the main_carousel_2.jpg file.

![](JPG/carousel2.png)

> **Important Note:** If there is no jpeg files extracted you may want to **clear all the browsing data** data in **Chrome** and repeat the process from Step1.
![](JPG/clear%20the%20history.png)

16. Observe and all the files extracted from the **HTTP stream**.


#### ![check](JPG/pngegg%20(1).png) You have successfully done Packet Sniffing for Image Capture and Extraction with Wireshark.

***

## **Task 5.4:** Capturing Packets with tcpdump

#### Let's get started with the Linux Desktop:
1. On the "**Remote Desktop Connection Manager**" left pane, 
click on the VM "**03 - Linux Client**" 

![](JPG/Screenshot_2.png)

2. You'll be presented with the "**Ubuntu Log-in screen**"; At the center of the screen, select the user "**Sophos**" and type the password: `Sophos1985`

![](JPG/Ubuntuxxxx.png)

> ![](JPG/output-onlinepngtools.png) **Note:** You may want to toggle the "Full-Screen View" in your browser to fit the Linux Desktop in your browser window.


### Let's begin with the Lab:

![](JPG/Linux%20Client%201.png)

3. Hoover your pointer to the **Application Dock** on the bottom of the Linux Desktop and launch the **Terminal Emulator**. 
![](JPG/Linux%20Terminal.png)



4. To capture packets for troubleshooting or analysis, tcpdump requires elevated permissions, so in the following examples most commands are prefixed with `sudo`.  
To begin, use the command:
```bash
sudo tcpdump -D
```
Or you can use: `tcpdump --list-interfaces` (`-D` for short) to see which interfaces are available for capture.

![](JPG/TCPDUMP.png)
In the example above, you can see all the interfaces available in my machine. The special interface any allows capturing in any active interface.

5. Let's use it to start capturing some packets. Capture all packets in any interface by running this command:

```bash
sudo tcpdump --interface any
```
In the output all the packets captured are shown like this:
![](JPG/TCPDUMP2.png)

6. Tcpdump continues to capture packets until it receives an interrupt signal. 
Stop the capturing by pressing `Ctrl+C`. 

7. To limit the number of packets captured and stop tcpdump, use the `-c` (for count) option:

```bash
sudo tcpdump -i any -c 5
```
In this case, tcpdump stopped capturing automatically after capturing five packets. 
![](JPG/TCPDUMP3.png)

> This is useful in different scenarios, for instance, if you're troubleshooting connectivity and capturing a few initial packets is enough. 

8. By default, tcpdump resolves IP addresses and ports into names, as shown in the previous example. When troubleshooting network issues, it is often easier to use the IP addresses and port numbers; disable name resolution by using the option `-n` and port resolution with `-nn`:
Type the following command:

```bash
sudo tcpdump -i any -c 5 -nn
```
##### Below you can see the two different output with and without name resolution for host-names and port-numbers.
![](JPG/TCPDUMP4.png)

##### One of tcpdump's most powerful features is its ability to filter the captured packets using a variety of parameters, such as s**ource and destination IP addresses**, **ports**, **protocols**, etc..  
Let's look at some of the most common ones.

9. To filter packets based on **protocol**, specifying the protocol in the command line. For example, capture **ICMP packets** only by using this command:

```bash
sudo tcpdump -i any -c5 icmp
```
10. In a different terminal, try to **ping** another machine:
```bash
ping 172.17.17.20
```
Back in the tcpdump capture, notice that tcpdump captures and displays only the **ICMP-related packets**

11. Now, Limit the captures to only packets related to a **specific host** by using the **host filter**:

```bash
$ sudo tcpdump -i any -c5 -nn host example.com
```
In this example, tcpdump captures and displays only packets moving to and from host `example.com`

12. In a different terminal, try to **ping** another machine:

```bash
ping 93.184.216.34
```
In the output you should see that TCPDUMP is only showing packets flowing from **example.com** which resolves into IP address: `93.184.216.34`

![](JPG/TCPDUMP5.png)


13. Now, let's filter packets based on the desired **service or port**, and **destination IP address**. For example, capture packets related to a web (**HTTP) service** destined to a specific site hosted elsewhere by using this command:

```bash
sudo tcpdump -i any -nn port 80 dst 10.1.1.250
```

14. In the **Applications** Menu, find and launch the Chrome Browser:  
**Applications > Internet > Chrome**

15. Now in **Chrome** navigate into this Blog site:

```bash 
http://10.1.1.250
```

16. Swift back to the terminal and see if TCPDUMP capture other traffic destined to ports and hosts other than the desired port and remote host.

![](JPG/TCPDUMP6.png)

> **Note:** You can also filter by source IP address by using `src` switch instead of `dst` 

##### Another useful feature provided by tcpdump is the ability to save the capture to a file so you can analyze the results later. This allows you to capture packets in batch mode overnight, for example, and verify the results in the morning. It also helps when there are too many packets to analyze since real-time capture can occur too fast.

17. To **save packets to a file** instead of displaying them on screen, use the option `-w` (for write).  
In the terminal type:

```bash
sudo tcpdump -i any -c20 -nn src 172.17.17.22 -w capture.pcap
```
This command saves the output in a file named capture.pcap.   
The **.pcap** extension stands for "**packet capture**" and is the convention for this file format.

![](JPG/TCPDUMP7.png)
As shown in this example, nothing gets displayed on-screen, and the capture finishes after capturing 20 packets, as per the option `-c20`. 

18. If you want some **feedback** to ensure packets are being captured, use the option `-v`.
Type the following command:

```bash
sudo tcpdump -i any -c50 -nn src 172.17.17.22 -w capture2.pcap -v
```
TCPdump will show how many packets are getting captured and finishes after capturing 50 packets, as per the option `-c50` in this case.


19. Now that you saved the two captures by creating two files in **binary format** (`capture.pcap`, `capture2.pcap`), you cannot simply open it with a text editor.   
To read the contents of the files, you can read and open them by executing tcpdump with the `-r` (for read) option.
Since you're no longer capturing the packets directly from the network interface, `sudo` is not required to read the files, tyoe:

```bash
tcpdump -r capture.pcap
```
Here is the output:
![](JPG/TCPDUMP8.png)


20. A more convenient way to open and read a pcap file generated by tcpdump is using Wireshark instead of tcpdump. Open the second pcap file by launching Wireshark from the terminal:

```bash
wireshark capture2.pcap
```
![](JPG/TCPDUMP9.png)

These basic features of tcpdump will help you get started with this powerful and versatile tool. 
To learn more, consult the tcpdump website and man pages:

https://www.tcpdump.org/

https://manpages.debian.org/stretch/tcpdump/tcpdump.8.en.html

![](JPG/TCPDUMP99.png)

The **tcpdump** command line interface provides **great flexibility** for capturing and analyzing network traffic. If you need a graphical tool to understand more complex flows, Wireshark is the choice.
  
One benefit of Wireshark is that it can read **.pcap** files captured by tcpdump. You can use tcpdump to capture packets in a remote machine that does not have a GUI and analyze the result file with Wireshark, but that is a topic for another day and support course.


***
## ![review](JPG/Review%2048.png) Review  ##

In this Lab you have: 
1.	Understand the uses of the **Process Monitor** Tool  
2.	Utilize **Wireshark** to capture and filter traffic 
3.	Utilize **TCPDUMP** to capture and filter traffic from the command line

***
***
### Before closing this page:
> Please remember to "Deallocate" the "HostVM" in the "Resource Tab" before closing this LAB, 
![](JPG/Deallocate%20the%20VM.png)
otherwise please continue to the next LAB.



