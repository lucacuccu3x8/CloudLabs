![](./media/image1.jpg){width="8.26388888888889in"
height="11.69513888888889in"}![](./media/image2.png){width="0.8979166666666667in"
height="0.15in"}![](./media/image3.png){width="4.4770844269466314in"
height="4.477083333333334in"}![](./media/image4.png){width="0.18055555555555555in"
height="0.2152777777777778in"}

Contents

[Introduction [4](#introduction)](#introduction)

[Prerequisites [4](#prerequisites)](#prerequisites)

[Workbook conventions [4](#workbook-conventions)](#workbook-conventions)

[Lab environment [4](#lab-environment)](#lab-environment)

[Environment overview [5](#environment-overview)](#environment-overview)

[User accounts [7](#user-accounts)](#user-accounts)

[Network diagram [8](#network-diagram)](#network-diagram)

[Lab 1: Windows Endpoint
[9](#lab-1-windows-endpoint)](#lab-1-windows-endpoint)

[Objectives [9](#objectives)](#objectives)

[Task 1.1: MSI logging
[9](#task-1.1-msi-logging)](#task-1.1-msi-logging)

[Task 1.2: Registry Editor
[10](#task-1.2-registry-editor)](#task-1.2-registry-editor)

[Task 1.3: Task Scheduler
[11](#task-1.3-task-scheduler)](#task-1.3-task-scheduler)

[Review [11](#review)](#review)

[Lab 2: Windows Server
[12](#lab-2-windows-server)](#lab-2-windows-server)

[Objectives [12](#objectives-1)](#objectives-1)

[Task 2.1: Group Policies
[12](#task-2.1-group-policies)](#task-2.1-group-policies)

[Review [13](#review-1)](#review-1)

[Lab 3: Active Directory
[14](#lab-3-active-directory)](#lab-3-active-directory)

[Objectives [14](#objectives-2)](#objectives-2)

[Task 3.1: OU, Group and User Configuration
[14](#task-3.1-ou-group-and-user-configuration)](#task-3.1-ou-group-and-user-configuration)

[Task 3.2: User and Group Attribute Troubleshooting
[14](#task-3.2-user-and-group-attribute-troubleshooting)](#task-3.2-user-and-group-attribute-troubleshooting)

[Review [15](#review-2)](#review-2)

[Lab 4: PowerShell [16](#lab-4-powershell)](#lab-4-powershell)

[Objectives [16](#objectives-3)](#objectives-3)

[Task 4.1: Basic Troubleshooting using PowerShell
[16](#task-4.1-basic-troubleshooting-using-powershell)](#task-4.1-basic-troubleshooting-using-powershell)

[Task 4.2: Troubleshoot PowerShell Script not executing
[17](#task-4.2-troubleshoot-powershell-script-not-executing)](#task-4.2-troubleshoot-powershell-script-not-executing)

[Review [17](#review-3)](#review-3)

[Lab 5: Tools [18](#lab-5-tools)](#lab-5-tools)

[Objectives [18](#objectives-4)](#objectives-4)

[Task 5.1: Debug Process Monitor Tool
[18](#task-5.1-debug-process-monitor-tool)](#task-5.1-debug-process-monitor-tool)

[Task 5.2: Debug Process Explorer Tool
[18](#task-5.2-debug-process-explorer-tool)](#task-5.2-debug-process-explorer-tool)

[Task 5.3: Wireshark Debugging
[19](#task-5.3-wireshark-debugging)](#task-5.3-wireshark-debugging)

[Review [19](#review-4)](#review-4)

[Lab 6: Networking [20](#lab-6-networking)](#lab-6-networking)

[Objectives [20](#objectives-5)](#objectives-5)

[Task 6.1: Display and understand routing table
[20](#task-6.1-display-and-understand-routing-table)](#task-6.1-display-and-understand-routing-table)

[Task 6.2: Configure a DHCP server
[21](#task-6.2-configure-a-dhcp-server)](#task-6.2-configure-a-dhcp-server)

[Task 6.3: Lookup and resolve various types of DNS records using
nslookup
[22](#task-6.3-lookup-and-resolve-several-types-of-dns-records-using-nslookup)](#task-6.3-lookup-and-resolve-several-types-of-dns-records-using-nslookup)

[Review [23](#review-5)](#review-5)

[Lab 7: Linux [24](#lab-7-linux)](#lab-7-linux)

[Objectives [24](#objectives-6)](#objectives-6)

[Task 7.1: Create, copy and rename a file before managing permissions
[24](#task-7.1-create-copy-and-rename-a-file-before-managing-permissions)](#task-7.1-create-copy-and-rename-a-file-before-managing-permissions)

[Task 7.2: Make edits and searches using vi
[25](#task-7.2-make-edits-and-searches-using-vi)](#task-7.2-make-edits-and-searches-using-vi)

[Task 7.3: Search using various grep commands through system files
[25](#task-7.3-search-using-various-grep-commands-through-system-files)](#task-7.3-search-using-various-grep-commands-through-system-files)

[Review [26](#review-6)](#review-6)

[Lab 8: Cryptography [27](#lab-8-cryptography)](#lab-8-cryptography)

[Objectives [27](#objectives-7)](#objectives-7)

[Task 8.1: Analyze and locate the CA of a website
[27](#task-8.1-analyze-and-locate-the-ca-of-a-website)](#task-8.1-analyze-and-locate-the-ca-of-a-website)

[Task 8.2: Generate a CSR using OpenSSL to prepare a certificate
[28](#task-8.2-generate-a-csr-using-openssl-to-prepare-a-certificate)](#task-8.2-generate-a-csr-using-openssl-to-prepare-a-certificate)

[Review [29](#review-7)](#review-7)

> © 2021 Sophos Limited. All rights reserved. No part of this document
> may be used or reproduced in any form or by any means without the
> prior written consent of Sophos.
>
> Sophos and the Sophos logo are registered trademarks of Sophos
> Limited. Other names, logos and marks mentioned in this document may
> be the trademarks or registered trademarks of Sophos Limited or their
> respective owners.
>
> While reasonable care has been taken in the preparation of this
> document, Sophos makes no warranties, conditions, or representations
> (whether express or implied) as to its completeness or accuracy. This
> document is subject to change at any time without notice.
>
> Sophos Limited is a company registered in England number 2096520,
> whose registered office is at The Pentagon, Abingdon Science Park,
> Abingdon, Oxfordshire, OX14 3YP.

# Introduction 

> These labs accompany the Sophos TSE Fundamentals Course. They are
> estimated
>
> to take 10 hours to complete.
>
> You should complete each section of labs when directed to do so in the
> training content. Throughout the labs there are prompts for
> information to be written down; you will require this information for
> the Lab review.
>
> If you need help or support at any point while completing the labs,
> please contact us at [TECHSUPTraining@sophos.com]{.underline} and one
> of the team will be able to assist you.
>
> Your Environment is hosted in CloudLabs and can be accessed through an
> Emulated RDP session in your Web browser.
>
> Use you Sophos Email address to register for the Lab and keep the
> confirmation Email to have faster access to your lab throughout the
> course.
>
> A native RDP connection is also available, but might require
> additional configuration, talk to your instructor should native RDP
> not work.
>
> Wait for all VM in the Hyper-V- Environment to complete startup before
> accessing your environment using the 'Lab Access' RDP Manager
> preconfigured on the Desktop of your virtual host.

## Prerequisites 

> ![](./media/image10.png){width="6.944444444444445e-2in"
> height="0.1423611111111111in"}![](./media/image10.png){width="6.944444444444445e-2in"
> height="0.1423611111111111in"}![](./media/image10.png){width="6.944444444444445e-2in"
> height="0.1423611111111111in"}Prior to taking this training, you
> should have:

General networking knowledge

Understanding of operating systems

Understanding of Active Directory

## Workbook conventions 

> This workbook uses the following conventions throughout:
>
> ![](./media/image10.png){width="6.944444444444445e-2in"
> height="0.1423611111111111in"} At the start of each lab is the
> learning objective, along with any requirements that must have been
> completed prior to starting the lab.
>
> ![](./media/image10.png){width="6.944444444444445e-2in"
> height="0.1423611111111111in"} Labs which cover larger subjects are
> divided into several tasks. Each task has a short description followed
> by the steps that are required to complete the task.
>
> ![](./media/image10.png){width="6.944444444444445e-2in"
> height="0.1423611111111111in"}![](./media/image10.png){width="6.944444444444445e-2in"
> height="0.1423611111111111in"} Short labs are presented as a single
> task.

Throughout the guide the following styles are used:

+---------------------------+------------------------------------------+
| > **Bold text**           | > ![](./media/ima                        |
|                           | ge10.png){width="6.944444444444445e-2in" |
|                           | > height="0.1423611111111111in"}         |
|                           | > Actions: On-screen elements that you   |
|                           | > interact with e.g., menu items,        |
|                           | > buttons, tick boxes, tabs, etc.        |
|                           | >                                        |
|                           | > ![](./media/ima                        |
|                           | ge10.png){width="6.944444444444445e-2in" |
|                           | > height="0.1423611111111111in"}         |
|                           | > Important points to note               |
+===========================+==========================================+
| > 'Single quotes'         | > On-screen elements that you do not     |
|                           | > interact with e.g., page titles, field |
|                           | > names, etc....                         |
+---------------------------+------------------------------------------+
| > Courier New font        | > Commands to be executed                |
+---------------------------+------------------------------------------+
| >                         | > Hyperlinks                             |
|  [Underlined]{.underline} |                                          |
+---------------------------+------------------------------------------+
| > \<variables\>           | > Variables will be shown between        |
|                           | > chevrons e.g., \<Red ID\>              |
+---------------------------+------------------------------------------+

## Lab environment 

> These labs are designed to be completed on the hosted
>
> Environment. Lab access will be provided by your instructor.
>
> Note: Since we are emulating common issues make sure to use the same
> password when working through labs. This will make it easier for your
> instructor in the event you require assistance during the lab. When
> creating a password, always use '**Sophos@1985**'. For backups, a more
> complex password is required, in that case, please use
> '**Sophos@1985Sophos@1985**'.

## Environment overview 

> The environment used to complete these labs is comprised of multiple
> computers, connected via a simple network.

+------------------+---------------------------------------------------+
| > **Computer**   | > **Description**                                 |
+==================+===================================================+
| >                | > This is the main network you will be using      |
| **SOPHOS.LOCAL** | > during the labs.                                |
|                  | >                                                 |
|                  | > Networks: 172.16.16.0/24, 192.168.16.0/24,      |
|                  | > 172,25,25,0/24                                  |
+------------------+---------------------------------------------------+
| > **LON-GW       | > This is a Sophos XG Firewall, and is the        |
| 1.SOPHOS.LOCAL** | > default gateway for the sophos.local network    |
|                  | > that has separate interfaces for multiple       |
|                  | > internal networks and WAN links.                |
|                  | >                                                 |
|                  | > IP addresses: 172.16.16.16, 10.1.1.100,         |
|                  | > 172.25.25.16, 172.30.30.16, 10.3.3.100,         |
|                  | > 10.100.100.65, 10.4.4.16                        |
|                  | >                                                 |
|                  | > Throughout this workbook this will be referred  |
|                  | > to as London Gateway 1                          |
+------------------+---------------------------------------------------+
| > **LON-GW       | > This is a Sophos XG Firewall, and is a gateway  |
| 2.SOPHOS.LOCAL** | > for the sophos.local network that has separate  |
|                  | > interfaces for multiple internal networks and   |
|                  | > WAN links.                                      |
|                  | >                                                 |
|                  | > IP addresses: 172.16.16.15, 10.1.1.115,         |
|                  | > 172.25.25.15, 172.30.30.15, 10.3.3.115,         |
|                  | > 10.100.100.66, 10.4.4.15                        |
|                  | >                                                 |
|                  | > Throughout this workbook this will be referred  |
|                  | > to as London Gateway 2                          |
+------------------+---------------------------------------------------+
| > **LON-D        | > This Windows 2016 Server is the domain          |
| C.SOPHOS.LOCAL** | > controller for the sophos.local domain. It runs |
|                  | > an SMTP server, webmail, DNS, Active Directory  |
|                  | > and a certificate authority. IP address:        |
|                  | > 172.16.16.10                                    |
|                  | >                                                 |
|                  | > Throughout this workbook this will be referred  |
|                  | > to as London DC                                 |
+------------------+---------------------------------------------------+
| > **LON-SRV      | > This Windows 2016 Server is being used as a     |
| 2.SOPHOS.LOCAL** | > client for these labs. IP address: 172.16.16.20 |
|                  | >                                                 |
|                  | > Throughout this workbook this will be referred  |
|                  | > to as London Server 2                           |
+------------------+---------------------------------------------------+
| > **INTRANE      | > This is a Debian Linux server running a simple  |
| T.SOPHOS.LOCAL** | > website. The server is located on a separate    |
|                  | > subnet.                                         |
|                  | >                                                 |
|                  | > IP address: 172.25.25.40, 172.25.25.41          |
|                  | >                                                 |
|                  | > Throughout this workbook this will be referred  |
|                  | > to as London Intranet                           |
+------------------+---------------------------------------------------+
| > **SOPHOS.DMZ** | > This is the DMZ for the lab network. Network:   |
|                  | >                                                 |
|                  | > 172.30.30.0/24                                  |
+------------------+---------------------------------------------------+
| > **ST           | > This is a Debian Linux server running a simple  |
| ORE.SOPHOS.DMZ** | > website. IP addresses: 172.30.30.50             |
|                  | >                                                 |
|                  | > Throughout this workbook this will be referred  |
|                  | > to as DMZ Website                               |
+------------------+---------------------------------------------------+
| > **NY-G         | > This is a Sophos XG Firewall, and is the        |
| W.SOPHOS.LOCAL** | > default gateway for the sophos.local network.   |
|                  | > IP addresses: 192.168.16.16, 172.25.25.17,      |
|                  | > 10.2.2.200                                      |
|                  | >                                                 |
|                  | > Throughout this workbook this will be referred  |
|                  | > to as New York Gateway                          |
+------------------+---------------------------------------------------+

+------------------+---------------------------------------------------+
| > **W            | > This is the network for the warehouse in New    |
| AREHOUSE.LOCAL** | > York. Network:                                  |
|                  | >                                                 |
|                  | > 172.25.25.0/24                                  |
+------------------+---------------------------------------------------+
| > **WAREHOUS     | > This is a Debian Linux server running a simple  |
| E.SOPHOS.LOCAL** | > website. The server is located on a separate    |
|                  | > subnet.                                         |
|                  | >                                                 |
|                  | > IP address: 172.25.25.60                        |
|                  | >                                                 |
|                  | > Throughout this workbook this will be referred  |
|                  | > to as New York Warehouse                        |
+------------------+---------------------------------------------------+
| >                | > This is a Debian Linux server which provides    |
| **INTERNET.WWW** | > central DNS for the sophos.local and            |
|                  | > sophos.local networks, as well as running a     |
|                  | > DHCP server, simple website, and certificate    |
|                  | > authority.                                      |
|                  | >                                                 |
|                  | > IP address: 10.1.1.250, 10.2.2.250,10.3.3.250   |
|                  | >                                                 |
|                  | > Throughout this workbook this will be referred  |
|                  | > to as Internet                                  |
+------------------+---------------------------------------------------+
| > **MPLS**       | > Network: 10.100.100.65/29                       |
+------------------+---------------------------------------------------+

## User accounts 

> The table below details the user accounts in the lab environment.

+------------------+-----------------+-------------+-----------------+
| > **Username**   | **Full name**   | *           | **Scope and     |
|                  |                 | *Password** | privileges**    |
+==================+=================+=============+=================+
| > **LAB\         | Administrator   | Sophos1985  | SOPHOS.LOCAL    |
| \administrator** |                 |             |                 |
|                  |                 |             | Domain          |
|                  |                 |             | administrator   |
+------------------+-----------------+-------------+-----------------+
| >                | John Smith      | Sophos1985  | SOPHOS.LOCAL    |
|  **LAB\\jsmith** |                 |             |                 |
|                  |                 |             | Domain User     |
+------------------+-----------------+-------------+-----------------+
| >                | Rob Brown       | Sophos1985  | SOPHOS.LOCAL    |
|  **LAB\\rbrown** |                 |             |                 |
|                  |                 |             | Domain User     |
+------------------+-----------------+-------------+-----------------+
| > **LAB\\spage** | Sally Page      | Sophos1985  | SOPHOS.LOCAL    |
|                  |                 |             |                 |
|                  |                 |             | Domain User     |
+------------------+-----------------+-------------+-----------------+
| > **LAB\\lfox**  | Lucy Fox        | Sophos1985  | SOPHOS.LOCAL    |
|                  |                 |             |                 |
|                  |                 |             | Domain User     |
+------------------+-----------------+-------------+-----------------+
| >                | Fred Rogers     | Sophos1985  | SOPHOS.LOCAL    |
| **LAB\\frogers** |                 |             |                 |
|                  |                 |             | Domain User     |
+------------------+-----------------+-------------+-----------------+
| > **root**       | Root            | Sophos1985  | DMZ Website     |
|                  |                 |             |                 |
|                  |                 |             | London Intranet |
|                  |                 |             |                 |
|                  |                 |             | New York        |
|                  |                 |             | Warehouse       |
|                  |                 |             |                 |
|                  |                 |             | Internet        |
|                  |                 |             |                 |
|                  |                 |             | Local           |
|                  |                 |             | Administrator   |
+------------------+-----------------+-------------+-----------------+
| > **sophos**     | Sophos          | Sophos1985  | DMZ Website     |
|                  |                 |             |                 |
|                  |                 |             | London Intranet |
|                  |                 |             |                 |
|                  |                 |             | New York        |
|                  |                 |             | Warehouse       |
|                  |                 |             |                 |
|                  |                 |             | Internet        |
|                  |                 |             |                 |
|                  |                 |             | Local User      |
+------------------+-----------------+-------------+-----------------+
| > **jbrown**     | Jim Brown       | Sophos1985  | Internet        |
|                  |                 |             |                 |
|                  |                 |             | Local User      |
+------------------+-----------------+-------------+-----------------+

## Network diagram 

> ![](./media/image11.png){width="4.51in" height="9.013334426946631in"}

# Lab 1: Windows Endpoint 

## Objectives 

> Upon successful completion of this lab, you will be able to:

1.  Use MsiExec to install and remove applications

2.  Perform a registry backup and restore

3.  Create a scheduled task to run a script

## Task 1.1: MSI logging 

> We will be looking at MSI files, their logs as well as use Windows
> Installer to uninstall.

+---+-------------------------------------------+-----------------------+
| > |                                           | > Notes               |
|   |                                           |                       |
| I |                                           |                       |
| n |                                           |                       |
| s |                                           |                       |
| t |                                           |                       |
| r |                                           |                       |
| u |                                           |                       |
| c |                                           |                       |
| t |                                           |                       |
| i |                                           |                       |
| o |                                           |                       |
| n |                                           |                       |
| s |                                           |                       |
+===+===========================================+=======================+
| > |                                           |                       |
|   |                                           |                       |
| ! |                                           |                       |
| [ |                                           |                       |
| ] |                                           |                       |
| ( |                                           |                       |
| . |                                           |                       |
| / |                                           |                       |
| m |                                           |                       |
| e |                                           |                       |
| d |                                           |                       |
| i |                                           |                       |
| a |                                           |                       |
| / |                                           |                       |
| i |                                           |                       |
| m |                                           |                       |
| a |                                           |                       |
| g |                                           |                       |
| e |                                           |                       |
| 1 |                                           |                       |
| 2 |                                           |                       |
| . |                                           |                       |
| p |                                           |                       |
| n |                                           |                       |
| g |                                           |                       |
| ) |                                           |                       |
| { |                                           |                       |
| w |                                           |                       |
| i |                                           |                       |
| d |                                           |                       |
| t |                                           |                       |
| h |                                           |                       |
| = |                                           |                       |
| " |                                           |                       |
| 0 |                                           |                       |
| . |                                           |                       |
| 5 |                                           |                       |
| 8 |                                           |                       |
| 9 |                                           |                       |
| 5 |                                           |                       |
| 8 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| i |                                           |                       |
| n |                                           |                       |
| " |                                           |                       |
| > |                                           |                       |
|   |                                           |                       |
| h |                                           |                       |
| e |                                           |                       |
| i |                                           |                       |
| g |                                           |                       |
| h |                                           |                       |
| t |                                           |                       |
| = |                                           |                       |
| " |                                           |                       |
| 0 |                                           |                       |
| . |                                           |                       |
| 5 |                                           |                       |
| 8 |                                           |                       |
| 9 |                                           |                       |
| 5 |                                           |                       |
| 8 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| 3 |                                           |                       |
| i |                                           |                       |
| n |                                           |                       |
| " |                                           |                       |
| } |                                           |                       |
| > |                                           |                       |
| > |                                           |                       |
|   |                                           |                       |
| O |                                           |                       |
| n |                                           |                       |
| > |                                           |                       |
|   |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
| L |                                           |                       |
| o |                                           |                       |
| n |                                           |                       |
| d |                                           |                       |
| o |                                           |                       |
| n |                                           |                       |
| > |                                           |                       |
|   |                                           |                       |
| D |                                           |                       |
| C |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > Open a web browser and navigate to      | > Proceed through any |
|   | > [https://172.16.16.16:4444]{.underline} | > warnings you        |
| * |                                           | > receive.            |
| * |                                           |                       |
| 1 |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > Login using the username 'admin'        | > Password is         |
|   |                                           | > Sophos@1985.        |
| * |                                           |                       |
| * |                                           |                       |
| 2 |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > On the left pane, navigate to Configure |                       |
|   | > \> VPN \> IPsec (remote access)         |                       |
| * |                                           |                       |
| * |                                           |                       |
| 3 |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
|   | > Click [Download client]{.underline}     |                       |
+---+-------------------------------------------+-----------------------+
| > | > Open Windows Explorer and navigate to   |                       |
|   | > the folder the installer was downloaded |                       |
| * | > to and extract the contents of the zip  |                       |
| * |                                           |                       |
| 4 |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > Hold shift and right click an empty     |                       |
|   | > area and select **Open Command window   |                       |
| * | > here**                                  |                       |
| * |                                           |                       |
| 5 |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > Run the following command to install    | > This will start the |
|   | > Sophos Connect 2.0:                     | > SophosConnect       |
| * | >                                         | > installer and       |
| * | > msiexec /i                              | > generate logs into  |
| 6 | >                                         | > a file named        |
| * | SophosConnect_2.0\_(IPsec_and_SSLVPN).msi | > Soph                |
| * | > /L\*v                                   | osConnectInstall.txt. |
|   | > C:                                      |                       |
|   | \\Windows\\Temp\\SophosConnectInstall.txt |                       |
+---+-------------------------------------------+-----------------------+
| > | > Follow the on-screen instructions to    |                       |
|   | > install Sophos Connect                  |                       |
| * |                                           |                       |
| * |                                           |                       |
| 7 |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > Use Windows Explorer to navigate to     |                       |
|   | > C:\\Windows\\Temp\\ and open the        |                       |
| * | > SophosConnectInstall log file           |                       |
| * |                                           |                       |
| 8 |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > Write down the line entry that          |                       |
|   | > indicates a successful or failed        |                       |
| * | > installation:                           |                       |
| * |                                           |                       |
| 9 |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > Write down the product code of this     |                       |
|   | > program:                                |                       |
| * |                                           |                       |
| * |                                           |                       |
| 1 |                                           |                       |
| 0 |                                           |                       |
| * |                                           |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > Uninstall PuTTY using the product code  |                       |
|   | > in the msiexec command:                 |                       |
| * | >                                         |                       |
| * | > msiexec /x \<Product Code\> /L\*v       |                       |
| 1 | >                                         |                       |
| 1 | > C:\\                                    |                       |
| * | Windows\\Temp\\SophosConnectUninstall.txt |                       |
| * |                                           |                       |
+---+-------------------------------------------+-----------------------+
| > | > You have analyzed MSI logs and used     |                       |
|   | > Windows Installer to manage PuTTy..     |                       |
| ! |                                           |                       |
| [ |                                           |                       |
| ] |                                           |                       |
| ( |                                           |                       |
| . |                                           |                       |
| / |                                           |                       |
| m |                                           |                       |
| e |                                           |                       |
| d |                                           |                       |
| i |                                           |                       |
| a |                                           |                       |
| / |                                           |                       |
| i |                                           |                       |
| m |                                           |                       |
| a |                                           |                       |
| g |                                           |                       |
| e |                                           |                       |
| 1 |                                           |                       |
| 3 |                                           |                       |
| . |                                           |                       |
| p |                                           |                       |
| n |                                           |                       |
| g |                                           |                       |
| ) |                                           |                       |
| { |                                           |                       |
| w |                                           |                       |
| i |                                           |                       |
| d |                                           |                       |
| t |                                           |                       |
| h |                                           |                       |
| = |                                           |                       |
| " |                                           |                       |
| 0 |                                           |                       |
| . |                                           |                       |
| 2 |                                           |                       |
| 1 |                                           |                       |
| 9 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| i |                                           |                       |
| n |                                           |                       |
| " |                                           |                       |
| > |                                           |                       |
|   |                                           |                       |
| h |                                           |                       |
| e |                                           |                       |
| i |                                           |                       |
| g |                                           |                       |
| h |                                           |                       |
| t |                                           |                       |
| = |                                           |                       |
| " |                                           |                       |
| 0 |                                           |                       |
| . |                                           |                       |
| 2 |                                           |                       |
| 1 |                                           |                       |
| 9 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| 4 |                                           |                       |
| i |                                           |                       |
| n |                                           |                       |
| " |                                           |                       |
| } |                                           |                       |
+---+-------------------------------------------+-----------------------+

## Task 1.2: Registry Editor 

> In this task we will create and modify a registry key as well as
> perform a backup and restore.

+---+------------------------------------------+-----------------------+
| > |                                          | > Notes               |
|   |                                          |                       |
| I |                                          |                       |
| n |                                          |                       |
| s |                                          |                       |
| t |                                          |                       |
| r |                                          |                       |
| u |                                          |                       |
| c |                                          |                       |
| t |                                          |                       |
| i |                                          |                       |
| o |                                          |                       |
| n |                                          |                       |
| s |                                          |                       |
+===+==========================================+=======================+
| > |                                          |                       |
|   |                                          |                       |
| ! |                                          |                       |
| [ |                                          |                       |
| ] |                                          |                       |
| ( |                                          |                       |
| . |                                          |                       |
| / |                                          |                       |
| m |                                          |                       |
| e |                                          |                       |
| d |                                          |                       |
| i |                                          |                       |
| a |                                          |                       |
| / |                                          |                       |
| i |                                          |                       |
| m |                                          |                       |
| a |                                          |                       |
| g |                                          |                       |
| e |                                          |                       |
| 1 |                                          |                       |
| 2 |                                          |                       |
| . |                                          |                       |
| p |                                          |                       |
| n |                                          |                       |
| g |                                          |                       |
| ) |                                          |                       |
| { |                                          |                       |
| w |                                          |                       |
| i |                                          |                       |
| d |                                          |                       |
| t |                                          |                       |
| h |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 9 |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| h |                                          |                       |
| e |                                          |                       |
| i |                                          |                       |
| g |                                          |                       |
| h |                                          |                       |
| t |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 9 |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| } |                                          |                       |
|   |                                          |                       |
| O |                                          |                       |
| n |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| L |                                          |                       |
| o |                                          |                       |
| n |                                          |                       |
| d |                                          |                       |
| o |                                          |                       |
| n |                                          |                       |
| D |                                          |                       |
| C |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Open Registry by typing 'regedit' in   |                       |
|   | > the Run Window                         |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Navigate to                            |                       |
|   | > 'Computer\\HKEY                        |                       |
| * | _LOCAL_MACHINE\\SOFTWARE\\WOW6432Node\\' |                       |
| * |                                          |                       |
| 2 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Right click **WOW6432Node** and create |                       |
|   | > a new key named 'TestRegistry'         |                       |
| * |                                          |                       |
| * |                                          |                       |
| 3 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Right click **TestRegistry** and       |                       |
|   | > create a new String Value named        |                       |
| * | > 'Setting'                              |                       |
| * |                                          |                       |
| 4 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Double click **Setting** and add value |                       |
|   | > data of 'Original data'                |                       |
| * |                                          |                       |
| * |                                          |                       |
| 5 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Right click **TestRegistry** and       |                       |
|   | > create a new DWORD Value named         |                       |
| * | > 'LogLevel'                             |                       |
| * |                                          |                       |
| 6 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Double click **LogLevel** and add      |                       |
|   | > value data of '3'                      |                       |
| * |                                          |                       |
| * |                                          |                       |
| 7 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Select **TestRegistry** on the left    | > This creates a      |
|   | > pane                                   | > backup that only    |
| * |                                          | > include content     |
| * |                                          | > under               |
| 8 |                                          | >                     |
| * |                                          | > HKLM\\SOFTWARE      |
| * |                                          | \\WOW6432Node\\TestRe |
|   |                                          | > gistry              |
+---+------------------------------------------+-----------------------+
| > | > Click on **File** on the top left and  |                       |
|   | > select **Export**                      |                       |
| * |                                          |                       |
| * |                                          |                       |
| 9 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Name the file export 'Test Registry    | > Name the file       |
|   | > Backup \<MM-DD-YYYY\>'and save this    | > accordingly with    |
| * | > file to the Desktop                    | > today's date        |
| * |                                          |                       |
| 1 |                                          |                       |
| 0 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Double click the **Setting** registry  |                       |
|   | > string and modify the value data to    |                       |
| * | > 'Modified data'                        |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 1 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Delete the **LogLevel** DWORD registry |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 2 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Open the Test Registry Backup file in  | > All registry backup |
|   | > Notepad                                | > files can be opened |
| * |                                          | > in a text editor.   |
| * |                                          | > You can confirm the |
| 1 |                                          | > contents before     |
| 3 |                                          | > importing the keys  |
| * |                                          | > back into the       |
| * |                                          | > registry            |
+---+------------------------------------------+-----------------------+
| > | > Note down the keys that were backed    |                       |
|   | > up:                                    |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 4 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Close Notepad                          |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 5 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Double click the Test Registry Backup  | > Confirm the warning |
|   | > file to import its contents to the     | > prompt              |
| * | > registry                               |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 6 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > In Registry Editor, navigate back to   |                       |
|   | > 'HKLM\\SOFTWARE\\WOW6432Node\\'        |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 7 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Note down the value data of the        |                       |
|   | > **Setting** registry key:              |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 8 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > You have successfully backed up and    |                       |
|   | > restored a registry key.               |                       |
| ! |                                          |                       |
| [ |                                          |                       |
| ] |                                          |                       |
| ( |                                          |                       |
| . |                                          |                       |
| / |                                          |                       |
| m |                                          |                       |
| e |                                          |                       |
| d |                                          |                       |
| i |                                          |                       |
| a |                                          |                       |
| / |                                          |                       |
| i |                                          |                       |
| m |                                          |                       |
| a |                                          |                       |
| g |                                          |                       |
| e |                                          |                       |
| 1 |                                          |                       |
| 3 |                                          |                       |
| . |                                          |                       |
| p |                                          |                       |
| n |                                          |                       |
| g |                                          |                       |
| ) |                                          |                       |
| { |                                          |                       |
| w |                                          |                       |
| i |                                          |                       |
| d |                                          |                       |
| t |                                          |                       |
| h |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 2 |                                          |                       |
| 1 |                                          |                       |
| 9 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| h |                                          |                       |
| e |                                          |                       |
| i |                                          |                       |
| g |                                          |                       |
| h |                                          |                       |
| t |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 2 |                                          |                       |
| 1 |                                          |                       |
| 9 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| } |                                          |                       |
+---+------------------------------------------+-----------------------+

## Task 1.3: Task Scheduler 

> In this task we will create a scheduled task to run a script at a
> specific time and date.

+---+------------------------------------------+-----------------------+
| > |                                          | > Notes               |
|   |                                          |                       |
| I |                                          |                       |
| n |                                          |                       |
| s |                                          |                       |
| t |                                          |                       |
| r |                                          |                       |
| u |                                          |                       |
| c |                                          |                       |
| t |                                          |                       |
| i |                                          |                       |
| o |                                          |                       |
| n |                                          |                       |
| s |                                          |                       |
+===+==========================================+=======================+
| > |                                          |                       |
|   |                                          |                       |
| ! |                                          |                       |
| [ |                                          |                       |
| ] |                                          |                       |
| ( |                                          |                       |
| . |                                          |                       |
| / |                                          |                       |
| m |                                          |                       |
| e |                                          |                       |
| d |                                          |                       |
| i |                                          |                       |
| a |                                          |                       |
| / |                                          |                       |
| i |                                          |                       |
| m |                                          |                       |
| a |                                          |                       |
| g |                                          |                       |
| e |                                          |                       |
| 1 |                                          |                       |
| 2 |                                          |                       |
| . |                                          |                       |
| p |                                          |                       |
| n |                                          |                       |
| g |                                          |                       |
| ) |                                          |                       |
| { |                                          |                       |
| w |                                          |                       |
| i |                                          |                       |
| d |                                          |                       |
| t |                                          |                       |
| h |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 9 |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| h |                                          |                       |
| e |                                          |                       |
| i |                                          |                       |
| g |                                          |                       |
| h |                                          |                       |
| t |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 9 |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| } |                                          |                       |
| > |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| O |                                          |                       |
| n |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| L |                                          |                       |
| o |                                          |                       |
| n |                                          |                       |
| d |                                          |                       |
| o |                                          |                       |
| n |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| D |                                          |                       |
| C |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Open Notepad and write down the        |                       |
|   | > following text:                        |                       |
| * | >                                        |                       |
| * | > echo \"Hello World\" \>                |                       |
| 1 | >                                        |                       |
| * | > C:\\Users\\A                           |                       |
| * | dministrator\\Desktop\\scheduledtask.txt |                       |
+---+------------------------------------------+-----------------------+
| > | > Save the file with the name script.bat |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 2 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Close Notepad                          |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 3 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Open Task Scheduler by typing          |                       |
|   | > 'taskschd' in the Run Window           |                       |
| * |                                          |                       |
| * |                                          |                       |
| 4 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > In the left-hand pane, click on **Task |                       |
|   | > Scheduler Library**                    |                       |
| * |                                          |                       |
| * |                                          |                       |
| 5 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > In the right-hand pane, click **Create |                       |
|   | > Task...**                              |                       |
| * |                                          |                       |
| * |                                          |                       |
| 6 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > In the 'Name' field, enter 'Create txt |                       |
|   | > file'                                  |                       |
| * |                                          |                       |
| * |                                          |                       |
| 7 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Select Run whether user is logged in   |                       |
|   | > or not                                 |                       |
| * |                                          |                       |
| * |                                          |                       |
| 8 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Select the Triggers tab                |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 9 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Click **New...**                       |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 0 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > In the 'Settings' section set the      |                       |
|   | > start time 5 minutes from the current  |                       |
| * | > time                                   |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 1 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Click **OK**                           |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 2 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Select the Actions tab                 |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 3 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Click **New...**                       |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 4 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > In the Program/script field browse to  |                       |
|   | > the previously created script.bat      |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 5 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Click **OK**                           |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 6 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Select the Settings tab                |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 7 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Select Run task as soon as possible    |                       |
|   | > after as scheduled start is missed     |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 8 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Click **OK**                           |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 1 |                                          |                       |
| 9 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Enter the Administrator password       |                       |
|   | > Sophos1985, then click **OK**          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 2 |                                          |                       |
| 0 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Wait for the scheduled start time and  |                       |
|   | > confirm a file named scheduledtask is  |                       |
| * | > created on the Desktop                 |                       |
| * |                                          |                       |
| 2 |                                          |                       |
| 1 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > You have successfully created a basic  |                       |
|   | > scheduled task                         |                       |
| ! |                                          |                       |
| [ |                                          |                       |
| ] |                                          |                       |
| ( |                                          |                       |
| . |                                          |                       |
| / |                                          |                       |
| m |                                          |                       |
| e |                                          |                       |
| d |                                          |                       |
| i |                                          |                       |
| a |                                          |                       |
| / |                                          |                       |
| i |                                          |                       |
| m |                                          |                       |
| a |                                          |                       |
| g |                                          |                       |
| e |                                          |                       |
| 1 |                                          |                       |
| 3 |                                          |                       |
| . |                                          |                       |
| p |                                          |                       |
| n |                                          |                       |
| g |                                          |                       |
| ) |                                          |                       |
| { |                                          |                       |
| w |                                          |                       |
| i |                                          |                       |
| d |                                          |                       |
| t |                                          |                       |
| h |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 2 |                                          |                       |
| 1 |                                          |                       |
| 9 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| h |                                          |                       |
| e |                                          |                       |
| i |                                          |                       |
| g |                                          |                       |
| h |                                          |                       |
| t |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 2 |                                          |                       |
| 1 |                                          |                       |
| 9 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| } |                                          |                       |
+---+------------------------------------------+-----------------------+

## Review 

> You have now successfully:

1.  Used MsiExec to install and remove applications

2.  Performed a registry backup and restore

3.  Created a scheduled task to launch Notepad

# Lab 2: Windows Server 

## Objectives 

> Upon successful completion of this lab, you will be able to:

1.  Review roles installed on a Windows Server

2.  Apply password complexity requirements using Group Policies

## Task 2.1: Group Policies 

> You have recently been given access to the Domain Controller. Your
> task is to force all users to set a password with a minimum length of
> 10.

+---+------------------------------------------+------------------------+
| > |                                          | > Notes                |
|   |                                          |                        |
| I |                                          |                        |
| n |                                          |                        |
| s |                                          |                        |
| t |                                          |                        |
| r |                                          |                        |
| u |                                          |                        |
| c |                                          |                        |
| t |                                          |                        |
| i |                                          |                        |
| o |                                          |                        |
| n |                                          |                        |
| s |                                          |                        |
+===+==========================================+========================+
| > |                                          |                        |
|   |                                          |                        |
| ! |                                          |                        |
| [ |                                          |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 4 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 5 |                                          |                        |
| 8 |                                          |                        |
| 4 |                                          |                        |
| 7 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 3 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 5 |                                          |                        |
| 8 |                                          |                        |
| 4 |                                          |                        |
| 7 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 3 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
|   |                                          |                        |
| O |                                          |                        |
| n |                                          |                        |
| * |                                          |                        |
| * |                                          |                        |
| L |                                          |                        |
| o |                                          |                        |
| n |                                          |                        |
| d |                                          |                        |
| o |                                          |                        |
| n |                                          |                        |
| D |                                          |                        |
| C |                                          |                        |
| * |                                          |                        |
| * |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Open Server Manager and select Manage  |                        |
|   | > \> Add Roles and Features              |                        |
| 1 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Read the 'Before you begin' message    |                        |
|   | > and click Next                         |                        |
| 2 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Keep 'Role-based or feature-based      |                        |
|   | > installation' selected and click Next  |                        |
| 3 | > twice                                  |                        |
+---+------------------------------------------+------------------------+
| > | > Note down the server roles installed   |                        |
|   | > on this server:                        |                        |
| 4 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Click Cancel to exit out of Add Roles  |                        |
|   | > and Features                           |                        |
| 5 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Open Group Policy Management           |                        |
|   |                                          |                        |
| 6 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Navigate to Forest: SOPHOS.LOCAL \>    |                        |
|   | > Domains \> SOPHOS.LOCAL                |                        |
| 7 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Right-click SOPHOS.LOCAL and select    |                        |
|   | > **Create a GPO in this domain and link |                        |
| 8 | > it here...**                           |                        |
+---+------------------------------------------+------------------------+
| > | > In the 'Name' field enter Password     |                        |
|   | > policy then hit **OK**                 |                        |
| 9 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Right-click Password policy and select |                        |
|   | > **Edit...**                            |                        |
| 1 |                                          |                        |
| 0 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Select Computer Configuration \>       |                        |
|   | > Windows Settings \> Security Settings  |                        |
| 1 | > \> Account Policies \> Password Policy |                        |
| 1 | > in the left-hand panel                 |                        |
+---+------------------------------------------+------------------------+
| > | > Double click Minimum password length   |                        |
|   |                                          |                        |
| 1 |                                          |                        |
| 2 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Select **Define this policy** and set  |                        |
|   | > the password length to 10 characters   |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Click **OK**                           |                        |
|   |                                          |                        |
| 1 |                                          |                        |
| 4 |                                          |                        |
+---+------------------------------------------+------------------------+
| ! | > You have successfully noted down the   |                        |
| [ | > installed features on a server and     |                        |
| ] | > created a group policy                 |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Review 

> You have now successfully:

1.  Reviewed roles installed on a Windows Server

2.  Applied password complexity requirements using Group Policies

# Lab 3: Active Directory 

## Objectives 

> Upon successful completion of this lab, you will be able to:

1.  Create OUs, groups, and users in Active Directory

2.  Modify and identify both user and group attributes

## Task 3.1: OU, Group and User Configuration 

> You have been assigned a task to setup a user, group and an OU in
> Active Directory:

+---+---+-------------------+-------------------+---+------------------------+
| > |   |                   |                   |   | > Notes                |
|   |   |                   |                   |   |                        |
| I |   |                   |                   |   |                        |
| n |   |                   |                   |   |                        |
| s |   |                   |                   |   |                        |
| t |   |                   |                   |   |                        |
| r |   |                   |                   |   |                        |
| u |   |                   |                   |   |                        |
| c |   |                   |                   |   |                        |
| t |   |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| o |   |                   |                   |   |                        |
| n |   |                   |                   |   |                        |
| s |   |                   |                   |   |                        |
+===+===+===================+===================+===+========================+
| ! |   |                   |                   |   |                        |
| [ |   |                   |                   |   |                        |
| ] |   |                   |                   |   |                        |
| ( |   |                   |                   |   |                        |
| . |   |                   |                   |   |                        |
| / |   |                   |                   |   |                        |
| m |   |                   |                   |   |                        |
| e |   |                   |                   |   |                        |
| d |   |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| a |   |                   |                   |   |                        |
| / |   |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| m |   |                   |                   |   |                        |
| a |   |                   |                   |   |                        |
| g |   |                   |                   |   |                        |
| e |   |                   |                   |   |                        |
| 1 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| . |   |                   |                   |   |                        |
| p |   |                   |                   |   |                        |
| n |   |                   |                   |   |                        |
| g |   |                   |                   |   |                        |
| ) |   |                   |                   |   |                        |
| { |   |                   |                   |   |                        |
| w |   |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| d |   |                   |                   |   |                        |
| t |   |                   |                   |   |                        |
| h |   |                   |                   |   |                        |
| = |   |                   |                   |   |                        |
| " |   |                   |                   |   |                        |
| 0 |   |                   |                   |   |                        |
| . |   |                   |                   |   |                        |
| 5 |   |                   |                   |   |                        |
| 8 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 7 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 3 |   |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| n |   |                   |                   |   |                        |
| " |   |                   |                   |   |                        |
| h |   |                   |                   |   |                        |
| e |   |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| g |   |                   |                   |   |                        |
| h |   |                   |                   |   |                        |
| t |   |                   |                   |   |                        |
| = |   |                   |                   |   |                        |
| " |   |                   |                   |   |                        |
| 0 |   |                   |                   |   |                        |
| . |   |                   |                   |   |                        |
| 5 |   |                   |                   |   |                        |
| 8 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 7 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 2 |   |                   |                   |   |                        |
| 3 |   |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| n |   |                   |                   |   |                        |
| " |   |                   |                   |   |                        |
| } |   |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| O |   |                   |                   |   |                        |
| n |   |                   |                   |   |                        |
| * |   |                   |                   |   |                        |
| * |   |                   |                   |   |                        |
| L |   |                   |                   |   |                        |
| o |   |                   |                   |   |                        |
| n |   |                   |                   |   |                        |
| d |   |                   |                   |   |                        |
| o |   |                   |                   |   |                        |
| n |   |                   |                   |   |                        |
| D |   |                   |                   |   |                        |
| C |   |                   |                   |   |                        |
| * |   |                   |                   |   |                        |
| * |   |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| > | > |                   |                   |   | > Create these OUs     |
|   |   |                   |                   |   | > under SOPHOS.LOCAL   |
| 1 | C |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | O |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | f |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | K |                   |                   |   |                        |
|   | , |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | C |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | , |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | I |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| > | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| 2 | C |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | - |                   |                   |   |                        |
|   | O |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | f |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | y |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | 5 |                   |                   |   |                        |
|   | 0 |                   |                   |   |                        |
|   | % |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | y |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | 4 |                   |                   |   |                        |
|   | 9 |                   |                   |   |                        |
|   | % |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | O |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | S |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | - |                   |                   |   |                        |
|   | O |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | y |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | K |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | A |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | v |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | C |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | V |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | v |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | I |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | A |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | y |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| > | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| 3 | C |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | - |                   |                   |   |                        |
|   | O |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
|   |   | **OU**            | > **User**        |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
|   |   | > Abingdon        | > UserA, UserB    |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
|   |   | > Vancouver       | > UserC, UserD    |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
|   |   | > Ahmedabad       | > UserE, UserF    |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| > | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| 4 | C |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | ' |                   |                   |   |                        |
|   | S |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | ' |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | A |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | O |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | A |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| > | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| 5 | C |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | , |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | ' |                   |                   |   |                        |
|   | F |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | ' |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | I |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | O |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | U |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | F |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| > | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| ! | Y |                   |                   |   |                        |
| [ | o |                   |                   |   |                        |
| ] | u |                   |                   |   |                        |
| ( | > |                   |                   |   |                        |
| . |   |                   |                   |   |                        |
| / | h |                   |                   |   |                        |
| m | a |                   |                   |   |                        |
| e | v |                   |                   |   |                        |
| d | e |                   |                   |   |                        |
| i | > |                   |                   |   |                        |
| a |   |                   |                   |   |                        |
| / | c |                   |                   |   |                        |
| i | r |                   |                   |   |                        |
| m | e |                   |                   |   |                        |
| a | a |                   |                   |   |                        |
| g | t |                   |                   |   |                        |
| e | e |                   |                   |   |                        |
| 1 | d |                   |                   |   |                        |
| 3 | > |                   |                   |   |                        |
| . |   |                   |                   |   |                        |
| p | O |                   |                   |   |                        |
| n | U |                   |                   |   |                        |
| g | s |                   |                   |   |                        |
| ) | , |                   |                   |   |                        |
| { | > |                   |                   |   |                        |
| w |   |                   |                   |   |                        |
| i | U |                   |                   |   |                        |
| d | s |                   |                   |   |                        |
| t | e |                   |                   |   |                        |
| h | r |                   |                   |   |                        |
| = | s |                   |                   |   |                        |
| " | , |                   |                   |   |                        |
| 0 | > |                   |                   |   |                        |
| . |   |                   |                   |   |                        |
| 2 | a |                   |                   |   |                        |
| 1 | n |                   |                   |   |                        |
| 9 | d |                   |                   |   |                        |
| 4 | > |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 | G |                   |                   |   |                        |
| 4 | r |                   |                   |   |                        |
| 4 | o |                   |                   |   |                        |
| 4 | u |                   |                   |   |                        |
| 4 | p |                   |                   |   |                        |
| 4 | s |                   |                   |   |                        |
| 4 | > |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 | i |                   |                   |   |                        |
| 4 | n |                   |                   |   |                        |
| 4 | > |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| i | A |                   |                   |   |                        |
| n | c |                   |                   |   |                        |
| " | t |                   |                   |   |                        |
| > | i |                   |                   |   |                        |
|   | v |                   |                   |   |                        |
| h | e |                   |                   |   |                        |
| e | > |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| g | D |                   |                   |   |                        |
| h | i |                   |                   |   |                        |
| t | r |                   |                   |   |                        |
| = | e |                   |                   |   |                        |
| " | c |                   |                   |   |                        |
| 0 | t |                   |                   |   |                        |
| . | o |                   |                   |   |                        |
| 2 | r |                   |                   |   |                        |
| 1 | y |                   |                   |   |                        |
| 9 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| n |   |                   |                   |   |                        |
| " |   |                   |                   |   |                        |
| } |   |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+

## Task 3.2: User and Group Attribute Troubleshooting 

> You have been asked to troubleshoot the following task in Active
> Directory:

+---+------------------------------------------+------------------------+
| > |                                          | > Notes                |
|   |                                          |                        |
| I |                                          |                        |
| n |                                          |                        |
| s |                                          |                        |
| t |                                          |                        |
| r |                                          |                        |
| u |                                          |                        |
| c |                                          |                        |
| t |                                          |                        |
| i |                                          |                        |
| o |                                          |                        |
| n |                                          |                        |
| s |                                          |                        |
+===+==========================================+========================+
| > |                                          |                        |
|   |                                          |                        |
| ! |                                          |                        |
| [ |                                          |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 4 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 5 |                                          |                        |
| 8 |                                          |                        |
| 4 |                                          |                        |
| 7 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 3 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 5 |                                          |                        |
| 8 |                                          |                        |
| 4 |                                          |                        |
| 7 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 3 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
| > |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| O |                                          |                        |
| n |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| * |                                          |                        |
| * |                                          |                        |
| L |                                          |                        |
| o |                                          |                        |
| n |                                          |                        |
| d |                                          |                        |
| o |                                          |                        |
| n |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| D |                                          |                        |
| C |                                          |                        |
| * |                                          |                        |
| * |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > List the distinguished name for        |                        |
|   | > 'UserA' and 'UserD':                   |                        |
| 1 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the Mail, UserPrincipalName |                        |
|   | > and the sAMAccountName attribute for   |                        |
| 2 | > user 'Jane Doe':                       |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the displayName, GroupID    |                        |
|   | > and Common Name for user 'Lucy Fox':   |                        |
| 3 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the objectGUID and          |                        |
|   | > Distinguished name for group 'Sales':  |                        |
| 4 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > You have successfully verified user    |                        |
|   | > and group attributes                   |                        |
| ! |                                          |                        |
| [ |                                          |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Review 

> You have now successfully:

1.  Created OUs, groups, and users in Active Directory

2.  Modified and identified both user and group attributes

# Lab 4: PowerShell 

## Objectives 

> Upon successful completion of this lab, you will be able to:

1.  Perform basic troubleshooting using PowerShell

2.  Troubleshoot an inoperable PowerShell script

## Task 4.1: Basic Troubleshooting using PowerShell 

> A customer wants to perform the following tasks with the help of
> PowerShell:

1.  List out statistics for the Network Connection

2.  Determine what commands are available for the Measure-Object command

3.  Verify the status of the 'ssh-agent' service

4.  List out the process which is consuming High CPU

+---+------------------------------------------+------------------------+
| > |                                          | > Notes                |
|   |                                          |                        |
| I |                                          |                        |
| n |                                          |                        |
| s |                                          |                        |
| t |                                          |                        |
| r |                                          |                        |
| u |                                          |                        |
| c |                                          |                        |
| t |                                          |                        |
| i |                                          |                        |
| o |                                          |                        |
| n |                                          |                        |
| s |                                          |                        |
+===+==========================================+========================+
| > |                                          |                        |
|   |                                          |                        |
| ! |                                          |                        |
| [ |                                          |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 4 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 5 |                                          |                        |
| 8 |                                          |                        |
| 4 |                                          |                        |
| 7 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 3 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 5 |                                          |                        |
| 8 |                                          |                        |
| 4 |                                          |                        |
| 7 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 2 |                                          |                        |
| 3 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
| > |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| O |                                          |                        |
| n |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| * |                                          |                        |
| * |                                          |                        |
| L |                                          |                        |
| o |                                          |                        |
| n |                                          |                        |
| d |                                          |                        |
| o |                                          |                        |
| n |                                          |                        |
| > |                                          |                        |
|   |                                          |                        |
| D |                                          |                        |
| C |                                          |                        |
| * |                                          |                        |
| * |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Open PowerShell and find the command   |                        |
|   | > to verify Network Statistics i.e.,     |                        |
| 1 | > Ethernet Name, Received Bytes,         |                        |
|   | > Received Unicast Packets, Sent Bytes,  |                        |
|   | > Sent Unicast Packets.                  |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the command and the         |                        |
|   | > returned output for the recorded       |                        |
| 2 | > 'Network Statistics':                  |                        |
+---+------------------------------------------+------------------------+
| > | > Research and list a few examples using |                        |
|   | > the Measure-Object command:            |                        |
| 3 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the command to verify the   |                        |
|   | > status of the service, 'ssh-agent':    |                        |
| 4 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Find out the command to verify which   |                        |
|   | > process is consuming High CPU:         |                        |
| 5 |                                          |                        |
+---+------------------------------------------+------------------------+
| ! | > You have researched and used various   |                        |
| [ | > PowerShell commands                    |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Task 4.2: Troubleshoot PowerShell Script not executing 

A customer has created test script 'Script.ps1' and wants to validate it
by executing it before running the actual debug. However, when the
customer executes 'Script.ps1', they are getting an error. Verify why
the customer is not able to execute the script.

+---+------------------------------------------+-----------------------+
| > |                                          | > Notes               |
|   |                                          |                       |
| I |                                          |                       |
| n |                                          |                       |
| s |                                          |                       |
| t |                                          |                       |
| r |                                          |                       |
| u |                                          |                       |
| c |                                          |                       |
| t |                                          |                       |
| i |                                          |                       |
| o |                                          |                       |
| n |                                          |                       |
| s |                                          |                       |
+===+==========================================+=======================+
| > |                                          |                       |
|   |                                          |                       |
| ! |                                          |                       |
| [ |                                          |                       |
| ] |                                          |                       |
| ( |                                          |                       |
| . |                                          |                       |
| / |                                          |                       |
| m |                                          |                       |
| e |                                          |                       |
| d |                                          |                       |
| i |                                          |                       |
| a |                                          |                       |
| / |                                          |                       |
| i |                                          |                       |
| m |                                          |                       |
| a |                                          |                       |
| g |                                          |                       |
| e |                                          |                       |
| 1 |                                          |                       |
| 2 |                                          |                       |
| . |                                          |                       |
| p |                                          |                       |
| n |                                          |                       |
| g |                                          |                       |
| ) |                                          |                       |
| { |                                          |                       |
| w |                                          |                       |
| i |                                          |                       |
| d |                                          |                       |
| t |                                          |                       |
| h |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 9 |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| h |                                          |                       |
| e |                                          |                       |
| i |                                          |                       |
| g |                                          |                       |
| h |                                          |                       |
| t |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 9 |                                          |                       |
| 5 |                                          |                       |
| 8 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| 3 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| } |                                          |                       |
| > |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| O |                                          |                       |
| n |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| L |                                          |                       |
| o |                                          |                       |
| n |                                          |                       |
| d |                                          |                       |
| o |                                          |                       |
| n |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| D |                                          |                       |
| C |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Open PowerShell and execute the script | > PowerShell scripts  |
|   | > by running the command:                | > are stored as .ps1  |
| * | >                                        | > files. By default,  |
| * | > & "C:\\Script.ps1"                     | > you cannot run a    |
| 4 |                                          | > script by just      |
| * |                                          | > double-clicking a   |
| * |                                          | > file. This protects |
|   |                                          | > your system from    |
|   |                                          | > accidentally        |
|   |                                          | > executing malicious |
|   |                                          | > scripts.            |
+---+------------------------------------------+-----------------------+
| > | > Write down the error displayed after   |                       |
|   | > executing the script:                  |                       |
| * |                                          |                       |
| * |                                          |                       |
| 5 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > Write down how you resolved the issue: |                       |
|   |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
| 6 |                                          |                       |
| * |                                          |                       |
| * |                                          |                       |
+---+------------------------------------------+-----------------------+
| > | > You have resolved an issue where       |                       |
|   | > PowerShell Scripts were not executing  |                       |
| ! |                                          |                       |
| [ |                                          |                       |
| ] |                                          |                       |
| ( |                                          |                       |
| . |                                          |                       |
| / |                                          |                       |
| m |                                          |                       |
| e |                                          |                       |
| d |                                          |                       |
| i |                                          |                       |
| a |                                          |                       |
| / |                                          |                       |
| i |                                          |                       |
| m |                                          |                       |
| a |                                          |                       |
| g |                                          |                       |
| e |                                          |                       |
| 1 |                                          |                       |
| 3 |                                          |                       |
| . |                                          |                       |
| p |                                          |                       |
| n |                                          |                       |
| g |                                          |                       |
| ) |                                          |                       |
| { |                                          |                       |
| w |                                          |                       |
| i |                                          |                       |
| d |                                          |                       |
| t |                                          |                       |
| h |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 2 |                                          |                       |
| 1 |                                          |                       |
| 9 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| > |                                          |                       |
|   |                                          |                       |
| h |                                          |                       |
| e |                                          |                       |
| i |                                          |                       |
| g |                                          |                       |
| h |                                          |                       |
| t |                                          |                       |
| = |                                          |                       |
| " |                                          |                       |
| 0 |                                          |                       |
| . |                                          |                       |
| 2 |                                          |                       |
| 1 |                                          |                       |
| 9 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| 4 |                                          |                       |
| i |                                          |                       |
| n |                                          |                       |
| " |                                          |                       |
| } |                                          |                       |
+---+------------------------------------------+-----------------------+

## Review 

> You have now successfully:

1.  Performed basic troubleshooting using PowerShell

2.  Troubleshot a PowerShell Script that was not executing

# Lab 5: Tools 

## Objectives 

> Upon successful completion of this lab, you will be able to:

1.  Understand the uses of the Process Monitor Tool

2.  Understand the uses of the Process Explorer Tool

3.  Utilize Wireshark to capture and filter traffic

## Task 5.1: Debug Process Monitor Tool 

> You have been given a task where you need to capture all events i.e.,
> Registry activity, File System activity, Network activity and Thread
> activity, while accessing a website from Google Chrome.

+---+------------------------------------------+------------------------+
|   | ![](./media/i                            |                        |
|   | mage14.png){width="0.5847222222222223in" |                        |
|   | height="0.5847222222222223in"}           |                        |
|   |                                          |                        |
|   | On **London DC**                         |                        |
+===+==========================================+========================+
| > | > Open Process Monitor and start a       |                        |
|   | > capture                                |                        |
| 1 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Open Google Chrome and browse any      |                        |
|   | > website                                |                        |
| 2 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Filter for Google Chrome processes and |                        |
|   | > all its subtrees.                      |                        |
| 3 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Note down all the PIDs used by Google  |                        |
|   | > Chrome:                                |                        |
| 4 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Save the filtered capture as a PML and |                        |
|   | > write down all the distinct types of   |                        |
| 5 | > events:                                |                        |
+---+------------------------------------------+------------------------+
| ! | > You have successfully debugged using   |                        |
| [ | > the Process Monitor Tool               |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Task 5.2: Debug Process Explorer Tool 

> You have been asked to debug information using the command prompt with
> the help of the Process Explorer tool

+---+------------------------------------------+------------------------+
|   | ![](./media/i                            |                        |
|   | mage14.png){width="0.5847222222222223in" |                        |
|   | height="0.5847222222222223in"}           |                        |
|   |                                          |                        |
|   | On **London DC**                         |                        |
+===+==========================================+========================+
| > | > Open the Process Explorer and run      |                        |
|   | > Command Prompt                         |                        |
| 1 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Find the Command Prompt process and    |                        |
|   | > check all the information i.e., PID,   |                        |
| 2 | > Company Name, CPU, Memory Usage:       |                        |
+---+------------------------------------------+------------------------+
| > | > Review all the available options       | > These options        |
|   |                                          | > include Kill         |
| 3 |                                          | > Process, Create      |
|   |                                          | >                      |
|   |                                          | > Dump, Virus Total    |
|   |                                          | > check, Restart,      |
|   |                                          | > Suspend,             |
|   |                                          | >                      |
|   |                                          | > Properties and       |
|   |                                          | > Verify Image         |
|   |                                          | > Signatures           |
+---+------------------------------------------+------------------------+
| > | > Save the filtered capture for Command  |                        |
|   | > prompt in Process Explorer Data (.txt) |                        |
| 4 | > format                                 |                        |
+---+------------------------------------------+------------------------+
| ! | > You have successfully performed a      |                        |
| [ | > debug using Process Explorer           |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Task 5.3: Wireshark Debugging 

> You have been asked to obtain the following information from a
> Wireshark capture:

-   Wireshark Filter by IP

-   Wireshark Filter by Port

-   Wireshark Filter by IP and Port

-   Mac Address Filter

-   Filter by URL

-   Trace TCP Stream for website communication

-   Filter out Destination IP address

+---+------------------------------------------+------------------------+
|   | ![](./media/i                            |                        |
|   | mage14.png){width="0.5847222222222223in" |                        |
|   | height="0.5847222222222223in"}           |                        |
|   |                                          |                        |
|   | On **London DC**                         |                        |
+===+==========================================+========================+
| > | > Open Wireshark start a packet capture  |                        |
|   | > and access any HTTPs based Website.    |                        |
| 1 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Note down and verify the commands used |                        |
|   | > to filter for the information outlined |                        |
| 2 | > in the task above:                     |                        |
+---+------------------------------------------+------------------------+
| > | > Save the capture in PCAP format after  |                        |
|   | > validating.                            |                        |
| 3 |                                          |                        |
+---+------------------------------------------+------------------------+
| ! | > You have successfully utilized filters |                        |
| [ | > with Wireshark                         |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Review 

> You have now successfully:

1.  Debugged using Process Monitor Tool

2.  Debugged using Process Explorer Tool

3.  Wireshark Debugging

# Lab 6: Networking 

## Objectives 

> Upon successful completion of this lab, you will be able to:

1.  Display the routing table from a Windows and Linux client

2.  Configure a DHCP server and observe the various negotiations and
    behavior in various scenarios.

3.  Lookup and resolve several types of DNS records using nslookup

## Task 6.1: Display and understand routing table 

> You have been given a task to review the routing table on two clients
> to validate which interfaces are in use and what path is taken. It was
> noticed that some clients were getting unresponsive pages and it is
> suspected there is a potential routing issue. In order to confirm what
> path is being taken it was advised to investigate the individual
> routing tables of two problematic clients as the DHCP server was
> confirmed to be set correctly.

+---+---+-------------------+-------------------+---+------------------------+
|   | ! |                   |                   |   |                        |
|   | [ |                   |                   |   |                        |
|   | ] |                   |                   |   |                        |
|   | ( |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 5 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | ) |                   |                   |   |                        |
|   | { |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | 0 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 5 |                   |                   |   |                        |
|   | 8 |                   |                   |   |                        |
|   | 9 |                   |                   |   |                        |
|   | 5 |                   |                   |   |                        |
|   | 8 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | 0 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 5 |                   |                   |   |                        |
|   | 8 |                   |                   |   |                        |
|   | 9 |                   |                   |   |                        |
|   | 5 |                   |                   |   |                        |
|   | 8 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | } |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | O |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | * |                   |                   |   |                        |
|   | * |                   |                   |   |                        |
|   | L |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | C |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | * |                   |                   |   |                        |
|   | * |                   |                   |   |                        |
+===+===+===================+===================+===+========================+
| > | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| 1 | O |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | y |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | f |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| > | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| 2 | W |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | x |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | - |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | f |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
|   |   | > **Host**        | > **Next Hop**    |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
|   |   | > 10.1.40.3       | > 172.17.17.16    |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
|   |   | > 172.17.17.34    | > On link         |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
|   |   | > 8.8.8.8         | > 172.17.17.16    |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| > | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| 3 | O |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | P |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | T |                   |                   |   |                        |
|   | T |                   |                   |   |                        |
|   | Y |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | * |                   |                   |   |                        |
|   | * |                   |                   |   |                        |
|   | S |                   |                   |   |                        |
|   | S |                   |                   |   |                        |
|   | H |                   |                   |   |                        |
|   | * |                   |                   |   |                        |
|   | * |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | ' |                   |                   |   |                        |
|   | L |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | x |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | C |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | ' |                   |                   |   |                        |
|   | , |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | 2 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 2 |                   |                   |   |                        |
|   | 2 |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | , |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | ' |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | ' |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | f |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | m |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | - |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| > | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
| 4 | W |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | x |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | - |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | f |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | y |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | 4 |                   |                   |   |                        |
|   | 9 |                   |                   |   |                        |
|   | % |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | y |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | : |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | 5 |                   |                   |   |                        |
|   | 0 |                   |                   |   |                        |
|   | % |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | H |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | N |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | x |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | H |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | g |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | y |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 0 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 4 |                   |                   |   |                        |
|   | 0 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | 2 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 2 |                   |                   |   |                        |
|   | 2 |                   |                   |   |                        |
|   | ( |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | ) |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | v |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | 2 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 3 |                   |                   |   |                        |
|   | 4 |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | 2 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 6 |                   |                   |   |                        |
|   | ( |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | h |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | ) |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | = |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | " |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | 8 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 8 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 8 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 8 |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | 2 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 7 |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
|   | 1 |                   |                   |   |                        |
|   | 6 |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | p |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | c |                   |                   |   |                        |
|   | k |                   |                   |   |                        |
|   | q |                   |                   |   |                        |
|   | u |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | r |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | y |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   | < |                   |                   |   |                        |
|   | / |                   |                   |   |                        |
|   | t |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | b |                   |                   |   |                        |
|   | l |                   |                   |   |                        |
|   | e |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+
| ! | > |                   |                   |   |                        |
| [ |   |                   |                   |   |                        |
| ] | Y |                   |                   |   |                        |
| ( | o |                   |                   |   |                        |
| . | u |                   |                   |   |                        |
| / | > |                   |                   |   |                        |
| m |   |                   |                   |   |                        |
| e | h |                   |                   |   |                        |
| d | a |                   |                   |   |                        |
| i | v |                   |                   |   |                        |
| a | e |                   |                   |   |                        |
| / | > |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| m | s |                   |                   |   |                        |
| a | u |                   |                   |   |                        |
| g | c |                   |                   |   |                        |
| e | c |                   |                   |   |                        |
| 1 | e |                   |                   |   |                        |
| 3 | s |                   |                   |   |                        |
| . | s |                   |                   |   |                        |
| p | f |                   |                   |   |                        |
| n | u |                   |                   |   |                        |
| g | l |                   |                   |   |                        |
| ) | l |                   |                   |   |                        |
| { | y |                   |                   |   |                        |
| w | > |                   |                   |   |                        |
| i |   |                   |                   |   |                        |
| d | a |                   |                   |   |                        |
| t | n |                   |                   |   |                        |
| h | a |                   |                   |   |                        |
| = | l |                   |                   |   |                        |
| " | y |                   |                   |   |                        |
| 0 | z |                   |                   |   |                        |
| . | e |                   |                   |   |                        |
| 2 | d |                   |                   |   |                        |
| 1 | > |                   |                   |   |                        |
| 9 |   |                   |                   |   |                        |
| 4 | a |                   |                   |   |                        |
| 4 | n |                   |                   |   |                        |
| 4 | d |                   |                   |   |                        |
| 4 | > |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 | u |                   |                   |   |                        |
| 4 | n |                   |                   |   |                        |
| 4 | d |                   |                   |   |                        |
| 4 | e |                   |                   |   |                        |
| 4 | r |                   |                   |   |                        |
| 4 | s |                   |                   |   |                        |
| 4 | t |                   |                   |   |                        |
| 4 | o |                   |                   |   |                        |
| 4 | o |                   |                   |   |                        |
| i | d |                   |                   |   |                        |
| n | > |                   |                   |   |                        |
| " |   |                   |                   |   |                        |
| h | r |                   |                   |   |                        |
| e | o |                   |                   |   |                        |
| i | u |                   |                   |   |                        |
| g | t |                   |                   |   |                        |
| h | i |                   |                   |   |                        |
| t | n |                   |                   |   |                        |
| = | g |                   |                   |   |                        |
| " | > |                   |                   |   |                        |
| 0 |   |                   |                   |   |                        |
| . | t |                   |                   |   |                        |
| 2 | a |                   |                   |   |                        |
| 1 | b |                   |                   |   |                        |
| 9 | l |                   |                   |   |                        |
| 4 | e |                   |                   |   |                        |
| 4 | s |                   |                   |   |                        |
| 4 | > |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 | o |                   |                   |   |                        |
| 4 | n |                   |                   |   |                        |
| 4 | > |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| 4 | b |                   |                   |   |                        |
| 4 | o |                   |                   |   |                        |
| 4 | t |                   |                   |   |                        |
| 4 | h |                   |                   |   |                        |
| 4 | > |                   |                   |   |                        |
| 4 |   |                   |                   |   |                        |
| i | L |                   |                   |   |                        |
| n | i |                   |                   |   |                        |
| " | n |                   |                   |   |                        |
| } | u |                   |                   |   |                        |
|   | x |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | a |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | > |                   |                   |   |                        |
|   |   |                   |                   |   |                        |
|   | W |                   |                   |   |                        |
|   | i |                   |                   |   |                        |
|   | n |                   |                   |   |                        |
|   | d |                   |                   |   |                        |
|   | o |                   |                   |   |                        |
|   | w |                   |                   |   |                        |
|   | s |                   |                   |   |                        |
|   | . |                   |                   |   |                        |
+---+---+-------------------+-------------------+---+------------------------+

## Task 6.2: Configure a DHCP server 

> You have been given a task to set up a new DHCP scope for the network
> 172.16.16.0/24 on the local domain controller. After creating the
> relevant scope, you must confirm the DHCP server was correctly
> responding to the requests, so evidence must be provided of the DHCP
> resolution.

+---+------------------------------------------+------------------------+
|   | > ![](./media/i                          |                        |
|   | mage15.png){width="0.5895833333333333in" |                        |
|   | > height="0.5895833333333333in"}         |                        |
|   | >                                        |                        |
|   | > On **London Client**                   |                        |
+===+==========================================+========================+
| > | > Open a windows command prompt and type | > Ensure interface     |
|   | > in the following:                      | > 'Ethernet 3' is      |
| 1 | >                                        | > enabled.             |
|   | > ipconfig /all                          |                        |
+---+------------------------------------------+------------------------+
| > | > Take note of the interface details of  | > Review the           |
|   | > 'Ethernet 3':                          | > Autoconfiguration    |
| 2 | >                                        | > IPv4 Address,        |
|   | > Ethernet adapter Ethernet 2:           | >                      |
|   | >                                        | > Default Gateway,     |
|   | > Connection-specific DNS Suffix . :     | > Subnet Mask, and DNS |
|   | >                                        | >                      |
|   | > Description . . . . . . . . . . . :    | > Servers              |
|   | > Microsoft Hyper-V Network Adapter #2   |                        |
|   | >                                        |                        |
|   | > Physical Address. . . . . . . . . :    |                        |
|   | > 00-15-5D-02-05-79                      |                        |
|   | >                                        |                        |
|   | > DHCP Enabled. . . . . . . . . . . : No |                        |
|   | >                                        |                        |
|   | > Autoconfiguration Enabled . . . . :    |                        |
|   | > Yes                                    |                        |
|   | >                                        |                        |
|   | > Link-local IPv6 Address . . . . . :    |                        |
|   | > fe80::98e7:9991:5b7b:ed0d%3(Preferred) |                        |
|   | >                                        |                        |
|   | > IPv4 Address. . . . . . . . . . . :    |                        |
|   | > 172.17.17.20(Preferred)                |                        |
|   | >                                        |                        |
|   | > Subnet Mask . . . . . . . . . . . :    |                        |
|   | > 255.255.255.0                          |                        |
|   | >                                        |                        |
|   | > Default Gateway . . . . . . . . . :    |                        |
|   | > 172.17.17.16                           |                        |
|   | >                                        |                        |
|   | > DHCPv6 IAID . . . . . . . . . . . :    |                        |
|   | > 117445981                              |                        |
|   | >                                        |                        |
|   | > DHCPv6 Client DUID. . . . . . . . :    |                        |
|   | > 0                                      |                        |
|   | 0-01-00-01-21-62-06-A6-00-50-56-2E-C6-24 |                        |
|   | >                                        |                        |
|   | > DNS Servers . . . . . . . . . . . :    |                        |
|   | > 172.16.16.10                           |                        |
|   | >                                        |                        |
|   | > 172.17.17.16                           |                        |
|   | >                                        |                        |
|   | > 10.1.1.250                             |                        |
|   | >                                        |                        |
|   | > NetBIOS over Tcpip. . . . . . . . :    |                        |
|   | > Enabled                                |                        |
+---+------------------------------------------+------------------------+

+---+------------------------------------------+------------------------+
|   | ![](./media/i                            |                        |
|   | mage14.png){width="0.5847222222222223in" |                        |
|   | height="0.5847222222222223in"}           |                        |
|   |                                          |                        |
|   | On **London DC**                         |                        |
+===+==========================================+========================+
| > | > Open the Windows 'Administrative       |                        |
|   | > Tools' from the Windows Start menu and |                        |
| 1 | > select **DHCP**                        |                        |
+---+------------------------------------------+------------------------+
| > | > Under the IPv4 dropdown, right click   |                        |
|   | > and create a new scope. Using the      |                        |
| 2 | > following information:                 |                        |
|   | >                                        |                        |
|   | > Name: Task6                            |                        |
|   | >                                        |                        |
|   | > Description: \<Optional\>              |                        |
|   | >                                        |                        |
|   | > Start IP address: 172.16.16.1          |                        |
|   | >                                        |                        |
|   | > End IP address: 172.16.16.50           |                        |
|   | >                                        |                        |
|   | > Subnet mask: 255.255.255.0             |                        |
|   | >                                        |                        |
|   | > Exclusions/Delay: \<Skip\>             |                        |
|   | >                                        |                        |
|   | > Lease Duration: 8 days                 |                        |
|   | >                                        |                        |
|   | > DHCP Options configure only the        |                        |
|   | > following:                             |                        |
|   |                                          |                        |
|   | -   Default Gateway (Router):            |                        |
|   |     > 172.16.16.16                       |                        |
|   |                                          |                        |
|   | -   DNS Parent domain: SOPHOS.LOCAL      |                        |
|   |                                          |                        |
|   | -   DNS Servers: 8.8.8.8                 |                        |
+---+------------------------------------------+------------------------+
| > | > Within Scope \[172.16.16.0\] Task6,    |                        |
|   | > **select Scope Options**, then right   |                        |
| 3 | > click and select **Configure           |                        |
|   | > Options**. Look and familiarize        |                        |
|   | > yourself with the available options.   |                        |
|   | > Identify and write down 5 different    |                        |
|   | > predefined options and their uses:     |                        |
+---+------------------------------------------+------------------------+

+---+------------------------------------------+------------------------+
|   | ![](./media/i                            |                        |
|   | mage15.png){width="0.5895833333333333in" |                        |
|   | height="0.5895833333333333in"}           |                        |
|   |                                          |                        |
|   | On **London Client**                     |                        |
+===+==========================================+========================+
| > | > Open Wireshark and run a capture on    | > (had to Enabler the  |
|   | > 'Ethernet 3'                           | > Ethernet 3)          |
| 1 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Open Command prompt and initiate a     | > (had to give it a    |
|   | > **DHCP release/renew**                 | > static ip address,   |
| 2 |                                          | > then selecting the   |
|   |                                          | > "obtain ip           |
|   |                                          | > automatically" from  |
|   |                                          | > GUI                  |
+---+------------------------------------------+------------------------+
| > | > Run ipconfig /all and compare the      |                        |
|   | > current details of Ethernet 3 details  |                        |
| 3 | > to when this command was previously    |                        |
|   | > run:                                   |                        |
+---+------------------------------------------+------------------------+
| > | > Open up Wireshark and filter for the   | > DORA request:        |
|   | > DHCP traffic only. Open each packet in | >                      |
| 4 | > the DHCP sequence to be familiar with  | > Discovery -- Client  |
|   | > each type of packet\'s being           | > sending Broadcast    |
|   | > requested.                             | >                      |
|   |                                          | > Offer -- Server      |
|   |                                          | > sending a reply      |
|   |                                          | >                      |
|   |                                          | > Request -- client    |
|   |                                          | > requesting ip Broad  |
|   |                                          | >                      |
|   |                                          | > ACK -- From server   |
+---+------------------------------------------+------------------------+
| > | > Write down what the server replied     |                        |
|   | > with for Option 51, Option 6, and      |                        |
| 5 | > Option 54:                             |                        |
|   |                                          |                        |
|   | +-----------------+------------------+   |                        |
|   | | Option 51       | > IP Address     |   |                        |
|   | |                 | > Lease Time --  |   |                        |
|   | |                 | > 8Days          |   |                        |
|   | +=================+==================+   |                        |
|   | | Option 6        | > Specify the    |   |                        |
|   | |                 | > DNS Server     |   |                        |
|   | |                 | > 8.8.8.8        |   |                        |
|   | +-----------------+------------------+   |                        |
|   | | Option 54       | > Specify IP     |   |                        |
|   | |                 | > DHCP Server    |   |                        |
|   | |                 | > Identity       |   |                        |
|   | +-----------------+------------------+   |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the source IP, destination  |                        |
|   | > IP, source mac address and destination |                        |
| 6 | > mac address of the DHCP Request:       |                        |
|   |                                          |                        |
|   | +-----------------+------------------+   |                        |
|   | | Source IP       | > 0.0.0.0 (Not   |   |                        |
|   | |                 | > assigned yet)  |   |                        |
|   | +=================+==================+   |                        |
|   | | Destination IP  | >                |   |                        |
|   | |                 |  255.255.255.255 |   |                        |
|   | |                 | > (broadcast)    |   |                        |
|   | +-----------------+------------------+   |                        |
|   | | Source MAC      | > 00155d02057a   |   |                        |
|   | | Address         |                  |   |                        |
|   | +-----------------+------------------+   |                        |
|   | | Destination MAC | > f              |   |                        |
|   | | Address         | f:ff:ff:ff:ff:ff |   |                        |
|   | +-----------------+------------------+   |                        |
|   |                                          |                        |
|   | > Why are these addresses used?          |                        |
|   |                                          |                        |
|   | 1.  means "any" or "unassigned",         |                        |
|   |     since **the source mac address       |                        |
|   |     (client) does not have an            |                        |
|   |     associated/configured IP address**.  |                        |
|   |                                          |                        |
|   | > 255.255.255.255 **It floods a DHCP     |                        |
|   | > Request message over the IP network**  |                        |
|   | >                                        |                        |
|   | > **using** a broadcast IP address       |                        |
|   | > (255.255. 255.255) in order to deliver |                        |
|   | > the DHCP Request message to all the    |                        |
|   | > DHCP servers on the same subnet        |                        |
|   | >                                        |                        |
|   | > Source Mac Address -- The Mac address  |                        |
|   | > of the client looking to get an ip     |                        |
|   | > assigned by any available DHCP server  |                        |
|   | > in the broadcast domain.               |                        |
|   | >                                        |                        |
|   | > ff-ff-ff-ff-ff-ff :Destination MAC     |                        |
|   | > Address -- A frame with a DHCP         |                        |
|   | > discovery/request is delivered and     |                        |
|   | > flooded to all available devices in    |                        |
|   | > the network (broadcast), in hope that  |                        |
|   | > a DHCP will reply and acknowledge the  |                        |
|   | > request for ip assignment.             |                        |
+---+------------------------------------------+------------------------+
| > | > Disable interface 'Ethernet 3'         |                        |
|   | >                                        |                        |
| 7 | > <https://winaero.                      |                        |
|   | com/disable-network-adapter-windows-10/> |                        |
|   | >                                        |                        |
|   | > or in cmd prompt:                      |                        |
|   | >                                        |                        |
|   | > netsh interface show interface         |                        |
|   | >                                        |                        |
|   | > netsh interface set interface          |                        |
|   | > "Ethernet 3" disable/enable            |                        |
|   | >                                        |                        |
|   | > or with Powershell:                    |                        |
|   | >                                        |                        |
|   | > get-net-adapter                        |                        |
|   | >                                        |                        |
|   | > Disable-Netadapter -Name "Ethernet 3"  |                        |
|   | >                                        |                        |
|   | > Enable-NetAdapter -Name \"your network |                        |
|   | > adapter name\"                         |                        |
+---+------------------------------------------+------------------------+
| ! | > You have now successfully analyzed     |                        |
| [ | > DHCP requests and created a DHCP scope |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

##  Task 6.3: Lookup and resolve several types of DNS records using nslookup 

> You have been given a task to display the routing table on two clients
> to validate which interfaces are being used. This must be verified on
> both London Client and Linux Client.
>
> ![](./media/image15.png){width="0.5895833333333333in"
> height="0.5895833333333333in"}

+---+---------------------------------------------+---------------------+
| > | > Open Wireshark and run a packet capture   |                     |
|   | > on 'Ethernet 2'                           |                     |
| 1 |                                             |                     |
+===+=============================================+=====================+
| > | > Open a command prompt and write down the  |                     |
|   | > DNS queries used for the following        |                     |
| 2 | > scenarios, using nslookup:                |                     |
|   |                                             |                     |
|   | +------------+----+--------------------+    |                     |
|   | | > **Des    | >  | > **Query Used**   |    |                     |
|   | | tination** | ** |                    |    |                     |
|   | |            | Re |                    |    |                     |
|   | |            | co |                    |    |                     |
|   | |            | rd |                    |    |                     |
|   | |            | >  |                    |    |                     |
|   | |            | Ty |                    |    |                     |
|   | |            | pe |                    |    |                     |
|   | |            | ** |                    |    |                     |
|   | +============+====+====================+    |                     |
|   | | > so       | A  | Nslookup -type A   |    |                     |
|   | | phos.local |    | Sophos.local       |    |                     |
|   | +------------+----+--------------------+    |                     |
|   | | > so       | A  | Nslookup -type A   |    |                     |
|   | | phos.local |    | 8.8.8.8            |    |                     |
|   | | > using    |    |                    |    |                     |
|   | | > DNS      |    |                    |    |                     |
|   | | > 8.8.8.8  |    |                    |    |                     |
|   | +------------+----+--------------------+    |                     |
|   | | >          | T  | Nslookup -type TXT |    |                     |
|   | | sophos.com | XT | Sophos.com         |    |                     |
|   | +------------+----+--------------------+    |                     |
+---+---------------------------------------------+---------------------+
| > | > Stop the Wireshark capture and run a      |                     |
|   | > filter to display only DNS queries and    |                     |
| 3 | > replies                                   |                     |
|   | >                                           |                     |
|   | > Filter: dns                               |                     |
+---+---------------------------------------------+---------------------+
| > | > Which DNS server was used to query        |                     |
|   | > sophos.com for txt records?               |                     |
| 4 | >                                           |                     |
|   | > Server: LON-DC-SOPHOS.LOCAL               |                     |
|   | >                                           |                     |
|   | > Address: 172.16.16.10                     |                     |
|   | >                                           |                     |
|   | > Why was this DNS server used?             |                     |
|   | >                                           |                     |
|   | > The first available DNS holding the       |                     |
|   | > information, however it is a              |                     |
|   | > Non-Authoritative DNS server for the      |                     |
|   | > zone.                                     |                     |
+---+---------------------------------------------+---------------------+
| > | > What server provided the authoritative    |                     |
|   | > answer that sophos.local is not           |                     |
| 5 | > responsible when using DNS 8.8.8.8?       |                     |
|   | >                                           |                     |
|   | > When querying                             |                     |
|   | >                                           |                     |
|   | > Nslookup -type=soa dns.google             |                     |
|   | >                                           |                     |
|   | > Querying the non authoritative            |                     |
|   | > ns1.zdns.google:                          |                     |
|   |                                             |                     |
|   | Nslookup -type=soa ns1.zdns.google          |                     |
|   |                                             |                     |
|   | The answer comes from:                      |                     |
|   |                                             |                     |
|   | Zdns.google                                 |                     |
|   |                                             |                     |
|   | > What does this mean?                      |                     |
|   | >                                           |                     |
|   | > An authoritative answer is when the DNS   |                     |
|   | > server hosting the primary copy of the    |                     |
|   | > DNS record responses to your lookup.      |                     |
|   | >                                           |                     |
|   | > When nslookup provided results by a       |                     |
|   | > server that is not the authoritative      |                     |
|   | > (primary) source. Typically, this means   |                     |
|   | > the result was provided by a server that  |                     |
|   | > held a cached copy of the DNS record.     |                     |
|   | > This is important because the DNS record  |                     |
|   | > may have been changed recently and the    |                     |
|   | > cached copy may not reflect the most      |                     |
|   | > up-to-date information.                   |                     |
|   | >                                           |                     |
|   | > https://www.                              |                     |
|   | meridianoutpost.com/resources/articles/comm |                     |
|   | and-line/nslookup.php#AuthoritativeResponse |                     |
+---+---------------------------------------------+---------------------+
| ! | > You have now successfully made various    |                     |
| [ | > DNS request types and analyzed their      |                     |
| ] | > packets.                                  |                     |
| ( |                                             |                     |
| . |                                             |                     |
| / |                                             |                     |
| m |                                             |                     |
| e |                                             |                     |
| d |                                             |                     |
| i |                                             |                     |
| a |                                             |                     |
| / |                                             |                     |
| i |                                             |                     |
| m |                                             |                     |
| a |                                             |                     |
| g |                                             |                     |
| e |                                             |                     |
| 1 |                                             |                     |
| 3 |                                             |                     |
| . |                                             |                     |
| p |                                             |                     |
| n |                                             |                     |
| g |                                             |                     |
| ) |                                             |                     |
| { |                                             |                     |
| w |                                             |                     |
| i |                                             |                     |
| d |                                             |                     |
| t |                                             |                     |
| h |                                             |                     |
| = |                                             |                     |
| " |                                             |                     |
| 0 |                                             |                     |
| . |                                             |                     |
| 2 |                                             |                     |
| 1 |                                             |                     |
| 9 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| i |                                             |                     |
| n |                                             |                     |
| " |                                             |                     |
| h |                                             |                     |
| e |                                             |                     |
| i |                                             |                     |
| g |                                             |                     |
| h |                                             |                     |
| t |                                             |                     |
| = |                                             |                     |
| " |                                             |                     |
| 0 |                                             |                     |
| . |                                             |                     |
| 2 |                                             |                     |
| 1 |                                             |                     |
| 9 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| 4 |                                             |                     |
| i |                                             |                     |
| n |                                             |                     |
| " |                                             |                     |
| } |                                             |                     |
+---+---------------------------------------------+---------------------+

## Review 

> You have now successfully:

1.  Displayed the routing table from a Windows and Linux Client

2.  Configured a DHCP server and observed the various negotiations and
    behavior

3.  Looked up and resolved several types of DNS records using nslookup

# Lab 7: Linux 

## Objectives 

> Upon successful completion of this lab, you will be able to:

1.  Create, copy, move, and rename files

2.  Manage file and folder permissions

3.  Make edits to files using the text editor vi

4.  Search through files using the text editor vi

5.  Search through system files using various grep commands

## Task 7.1: Create, copy, and rename a file before managing permissions 

> You have been given a task to create two separate directories with two
> identical files. However, one file, 'file1b.log' requires different
> permissions than the original file. The 'file1b.log' requires file
> owner full permissions, the 'games' group read and execute
> permissions, and all others execute permissions only.

+---+------------------------------------------+------------------------+
|   | ![](./media/i                            |                        |
|   | mage15.png){width="0.5895833333333333in" |                        |
|   | height="0.5895833333333333in"}           |                        |
|   |                                          |                        |
|   | On **London Client**                     |                        |
+===+==========================================+========================+
| > | > Open PuTTY and SSH to the 'Linux       | > Password is          |
|   | > Client', 172.17.17.22 as the user      | > Sophos1985           |
| 1 | > 'sophos'                               |                        |
+---+------------------------------------------+------------------------+
| > | > Attempt to create two directories in   | > You will receive an  |
|   | > the /var directory, named task7a and   | > error 'Permission    |
| 2 | > task7b                                 | > denied'              |
+---+------------------------------------------+------------------------+
| > | > Set the proper permissions to allow    |                        |
|   | > the user 'sophos' and all others to    |                        |
| 3 | > write in the /var directory            |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the command(s) used to give | > **Hint:** You must   |
|   | > sufficient permissions to the /var     | > login as the file    |
| 4 | > directory:                             | > owner or root user   |
|   | >                                        | > to modify the        |
|   | > Chmod 773 /var                         | > permissions of a     |
|   |                                          | > file or directory    |
|   |                                          | >                      |
|   |                                          | > Password for root,   |
|   |                                          | > is 'Sophos1985'      |
+---+------------------------------------------+------------------------+
| > | > Attempt to create the two directories  | > The directory names  |
|   | > in /var directory again                | > should be 'task7a'   |
| 5 | >                                        | > and 'task7b'         |
|   | > /var# mkdir task7a task7b              |                        |
+---+------------------------------------------+------------------------+
| > | > As the user, 'sophos', create a file   |                        |
|   | > in /var/task7a/ named, 'file1.log'     |                        |
| 6 | > with the following content:            |                        |
|   | >                                        |                        |
|   | > This content is from file1             |                        |
|   | >                                        |                        |
|   | > This is line 2                         |                        |
|   | >                                        |                        |
|   | > /var# echo -e "This content is from    |                        |
|   | > file1\\nThis is line 2" \>             |                        |
|   | > task7a/file1.log                       |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the command(s) used to      | > Try to perform this  |
|   | > create the file and the content of     | > step as efficient as |
| 7 | > 'file1.log'                            | > possible             |
|   | >                                        |                        |
|   | > : /var# echo -e "This content is from  |                        |
|   | > file1\\nThis is line 2" \>             |                        |
|   | > task7a/file1.log                       |                        |
|   | >                                        |                        |
|   | > Cat /var/task7a/file1.log              |                        |
+---+------------------------------------------+------------------------+
| > | > Create a copy of /var/task7a/file1.log |                        |
|   | > and save it to /var/task7b. Then       |                        |
| 8 | > rename the /var/task7b/file1.log to    |                        |
|   | > file1b.log.                            |                        |
|   | >                                        |                        |
|   | > /var# cp task7a/file1.log task7b/ &&   |                        |
|   | > mv task7b/file1.log task7b/file1b.log  |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the command(s) used to copy |                        |
|   | > the file:                              |                        |
| 9 | >                                        |                        |
|   | > /var# cp task7a/file1.log task7b/ &&   |                        |
|   | > mv task7b/file1.log task7b/file1b.log  |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the command(s) used to      |                        |
|   | > rename the file:                       |                        |
| 1 |                                          |                        |
| 0 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Set the permissions of the file        | > **Hint:** To modify  |
|   | > 'file1b.log' to the following          | > the file you must be |
| 8 | > parameters:                            | > the file owner or    |
|   | >                                        | > group owner.         |
|   | > -rwxr-x\--x 1 sophos staff 42          |                        |
|   | > \<timestamp\> file1b.log               |                        |
+---+------------------------------------------+------------------------+
| 9 | > Write down the command(s) used to set  |                        |
| . | > the permissions of file1b.log:         |                        |
|   |                                          |                        |
|   | \> Chmod 711 file1b.log                  |                        |
|   |                                          |                        |
|   | > \# chown Sophos:staff file1b.log       |                        |
+---+------------------------------------------+------------------------+
| ! | > You have successfully created, copied, |                        |
| [ | > renamed, and modified file             |                        |
| ] | > permissions.                           |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Task 7.2: Make edits and searches using vi 

> You have been given a task where the administrator requires you to add
> additional lines to the file '/var/file1b.log' to diagnose an issue.
> It was suggested to use vi as there is no GUI on the Linux machine.
> Once complete, you must then search the file using a string and make a
> final line edit.

+---+------------------------------------------+------------------------+
|   | > ![](./media/i                          |                        |
|   | mage15.png){width="0.5895833333333333in" |                        |
|   | > height="0.5895833333333333in"}         |                        |
|   | >                                        |                        |
|   | > On **London Client**                   |                        |
+===+==========================================+========================+
| > | > Append the following lines to the      | > Case sensitivity is  |
|   | > bottom of '/var/file1b.log' using vi   | > important in Linux.  |
| 1 | > and save the file:                     |                        |
|   | >                                        |                        |
|   | > This is Line 3                         |                        |
|   | >                                        |                        |
|   | > This is LINE 4 This is line 5          |                        |
+---+------------------------------------------+------------------------+
| > | > While still in vi, enter in the '/' to |                        |
|   | > run a search within the file. Enter in |                        |
| 2 | > /line and hit enter to search. Press   |                        |
|   | > 'n' to jump between the search hits.   |                        |
|   | > Observe and take note of the cursor    |                        |
|   | > position.                              |                        |
+---+------------------------------------------+------------------------+
| > | > Write down why the search/cursor only  |                        |
|   | > jumps to line 2 and line 5 but none of |                        |
| 3 | > the others:                            |                        |
|   | >                                        |                        |
|   | > The reason is because the search is    |                        |
|   | > case sensitive -- only line with exact |                        |
|   | > string match will be shown by the      |                        |
|   | > search.                                |                        |
+---+------------------------------------------+------------------------+
| > | > Edit line 1 using vi and change the    |                        |
|   | > first line to:                         |                        |
| 4 | >                                        |                        |
|   | > This content is from file1b.log',      |                        |
+---+------------------------------------------+------------------------+
| > | > Write the changes and quit vi editor.  |                        |
|   | > Confirm the changes were successfully  |                        |
| 5 | > made have been saved.                  |                        |
+---+------------------------------------------+------------------------+
| ! | > You have successfully appended lines,  |                        |
| [ | > searched, and made file content        |                        |
| ] | > updates using vi.                      |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Task 7.3: Search using various grep commands through system files 

> You have been asked to gather all system logs for an event on January
> 22^nd^. The issue was reported at 7:15 AM but to ensure all the
> relevant logs are collected, you were tasked to gather everything that
> occurred on between 0700 and 0759. Understanding that it is your
> first-time searching content, your manager has provided you with a
> series of grep commands for practice.

+---+---+---+-----------------------+-----------+---+--------------------------+
|   | ! |   |                       |           |   |                          |
|   | [ |   |                       |           |   |                          |
|   | ] |   |                       |           |   |                          |
|   | ( |   |                       |           |   |                          |
|   | . |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | 1 |   |                       |           |   |                          |
|   | 5 |   |                       |           |   |                          |
|   | . |   |                       |           |   |                          |
|   | p |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | ) |   |                       |           |   |                          |
|   | { |   |                       |           |   |                          |
|   | w |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | = |   |                       |           |   |                          |
|   | " |   |                       |           |   |                          |
|   | 0 |   |                       |           |   |                          |
|   | . |   |                       |           |   |                          |
|   | 5 |   |                       |           |   |                          |
|   | 8 |   |                       |           |   |                          |
|   | 9 |   |                       |           |   |                          |
|   | 5 |   |                       |           |   |                          |
|   | 8 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | " |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | = |   |                       |           |   |                          |
|   | " |   |                       |           |   |                          |
|   | 0 |   |                       |           |   |                          |
|   | . |   |                       |           |   |                          |
|   | 5 |   |                       |           |   |                          |
|   | 8 |   |                       |           |   |                          |
|   | 9 |   |                       |           |   |                          |
|   | 5 |   |                       |           |   |                          |
|   | 8 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | 3 |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | " |   |                       |           |   |                          |
|   | } |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | O |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | * |   |                       |           |   |                          |
|   | * |   |                       |           |   |                          |
|   | L |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | C |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | * |   |                       |           |   |                          |
|   | * |   |                       |           |   |                          |
+===+===+===+=======================+===========+===+==========================+
| > | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
| 1 | C |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | y |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | * |   |                       |           |   |                          |
|   | * |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | v |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | k |   |                       |           |   |                          |
|   | 7 |   |                       |           |   |                          |
|   | b |   |                       |           |   |                          |
|   | * |   |                       |           |   |                          |
|   | * |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
| > | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
| 2 | R |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | f |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | w |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | k |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | f |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | f |   |                       |           |   |                          |
|   | f |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | p |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | f |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | : |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   | > |                       | *         |   |                          |
|   |   |   |                       | *Output** |   |                          |
|   |   | * |                       |           |   |                          |
|   |   | * |                       |           |   |                          |
|   |   | C |                       |           |   |                          |
|   |   | o |                       |           |   |                          |
|   |   | m |                       |           |   |                          |
|   |   | m |                       |           |   |                          |
|   |   | a |                       |           |   |                          |
|   |   | n |                       |           |   |                          |
|   |   | d |                       |           |   |                          |
|   |   | * |                       |           |   |                          |
|   |   | * |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   | > |                       | > None,   |   |                          |
|   |   |   |                       | > grep is |   |                          |
|   |   | g |                       | > case    |   |                          |
|   |   | r |                       | > s       |   |                          |
|   |   | e |                       | ensitive! |   |                          |
|   |   | p |                       |           |   |                          |
|   |   | > |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | ' |                       |           |   |                          |
|   |   | l |                       |           |   |                          |
|   |   | i |                       |           |   |                          |
|   |   | n |                       |           |   |                          |
|   |   | e |                       |           |   |                          |
|   |   | > |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | 4 |                       |           |   |                          |
|   |   | ' |                       |           |   |                          |
|   |   | > |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | f |                       |           |   |                          |
|   |   | i |                       |           |   |                          |
|   |   | l |                       |           |   |                          |
|   |   | e |                       |           |   |                          |
|   |   | 1 |                       |           |   |                          |
|   |   | b |                       |           |   |                          |
|   |   | . |                       |           |   |                          |
|   |   | l |                       |           |   |                          |
|   |   | o |                       |           |   |                          |
|   |   | g |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   | > |                       | > -i      |   |                          |
|   |   |   |                       | > tells   |   |                          |
|   |   | g |                       | > grep to |   |                          |
|   |   | r |                       | > skip    |   |                          |
|   |   | e |                       | > case    |   |                          |
|   |   | p |                       | >         |   |                          |
|   |   | > |                       | sensitive |   |                          |
|   |   |   |                       | > search  |   |                          |
|   |   | - |                       | > in      |   |                          |
|   |   | i |                       | >         |   |                          |
|   |   | > |                       | arguments |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | ' |                       |           |   |                          |
|   |   | l |                       |           |   |                          |
|   |   | i |                       |           |   |                          |
|   |   | n |                       |           |   |                          |
|   |   | e |                       |           |   |                          |
|   |   | > |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | 4 |                       |           |   |                          |
|   |   | ' |                       |           |   |                          |
|   |   | > |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | f |                       |           |   |                          |
|   |   | i |                       |           |   |                          |
|   |   | l |                       |           |   |                          |
|   |   | e |                       |           |   |                          |
|   |   | 1 |                       |           |   |                          |
|   |   | b |                       |           |   |                          |
|   |   | . |                       |           |   |                          |
|   |   | l |                       |           |   |                          |
|   |   | o |                       |           |   |                          |
|   |   | g |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   | > |                       | > Output  |   |                          |
|   |   |   |                       | > the     |   |                          |
|   |   | g |                       | > search  |   |                          |
|   |   | r |                       | > for     |   |                          |
|   |   | e |                       | > e       |   |                          |
|   |   | p |                       | verything |   |                          |
|   |   | > |                       | > else    |   |                          |
|   |   |   |                       | >         |   |                          |
|   |   | - |                       | excluding |   |                          |
|   |   | v |                       | > the     |   |                          |
|   |   | > |                       | >         |   |                          |
|   |   |   |                       |  matching |   |                          |
|   |   | f |                       | >         |   |                          |
|   |   | i |                       | argument. |   |                          |
|   |   | l |                       | > ca      |   |                          |
|   |   | e |                       | se/string |   |                          |
|   |   | 1 |                       |           |   |                          |
|   |   | b |                       |           |   |                          |
|   |   | . |                       |           |   |                          |
|   |   | l |                       |           |   |                          |
|   |   | o |                       |           |   |                          |
|   |   | g |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   | > |                       | > Show    |   |                          |
|   |   |   |                       | >         |   |                          |
|   |   | g |                       |  multiple |   |                          |
|   |   | r |                       | >         |   |                          |
|   |   | e |                       |  matching |   |                          |
|   |   | p |                       | >         |   |                          |
|   |   | > |                       |  searches |   |                          |
|   |   |   |                       | > in one  |   |                          |
|   |   | - |                       | >         |   |                          |
|   |   | e |                       |  command. |   |                          |
|   |   | > |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | ' |                       |           |   |                          |
|   |   | L |                       |           |   |                          |
|   |   | i |                       |           |   |                          |
|   |   | n |                       |           |   |                          |
|   |   | e |                       |           |   |                          |
|   |   | ' |                       |           |   |                          |
|   |   | > |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | - |                       |           |   |                          |
|   |   | e |                       |           |   |                          |
|   |   | > |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | ' |                       |           |   |                          |
|   |   | L |                       |           |   |                          |
|   |   | I |                       |           |   |                          |
|   |   | N |                       |           |   |                          |
|   |   | E |                       |           |   |                          |
|   |   | ' |                       |           |   |                          |
|   |   | > |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   |   | f |                       |           |   |                          |
|   |   | i |                       |           |   |                          |
|   |   | l |                       |           |   |                          |
|   |   | e |                       |           |   |                          |
|   |   | 1 |                       |           |   |                          |
|   |   | b |                       |           |   |                          |
|   |   | . |                       |           |   |                          |
|   |   | l |                       |           |   |                          |
|   |   | o |                       |           |   |                          |
|   |   | g |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
| > |   |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
| 3 |   |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
|   |   |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
| > | > |   |                       |           |   | > Confirm this file only |
|   |   |   |                       |           |   | > contains syslog        |
| 4 | R |   |                       |           |   | > messages between 7 AM  |
|   | u |   |                       |           |   | > to 8 AM on Jan 22^nd^. |
|   | n |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | f |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | y |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | J |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | y |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | 2 |   |                       |           |   |                          |
|   | 2 |   |                       |           |   |                          |
|   | ^ |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | ^ |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | 7 |   |                       |           |   |                          |
|   | ^ |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | ^ |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | . |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | S |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | p |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | f |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | ' |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | v |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | k |   |                       |           |   |                          |
|   | 7 |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | y |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | J |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | 2 |   |                       |           |   |                          |
|   | 2 |   |                       |           |   |                          |
|   | . |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | ' |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
| > | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
| 5 | W |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | w |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | w |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | ( |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | ) |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | w |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | p |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | p |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | 5 |   |                       |           |   |                          |
|   | 4 |   |                       |           |   |                          |
|   | : |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | S |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | ' |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | v |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | y |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | d |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | v |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | b |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | y |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | m |   |                       |           |   |                          |
|   | . |   |                       |           |   |                          |
|   | . |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | h |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | p |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | c |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | y |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | b |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | k |   |                       |           |   |                          |
|   | ! |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | G |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | p |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | " |   |                       |           |   |                          |
|   | J |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | n |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | 2 |   |                       |           |   |                          |
|   | 2 |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | 0 |   |                       |           |   |                          |
|   | 7 |   |                       |           |   |                          |
|   | : |   |                       |           |   |                          |
|   | \ |   |                       |           |   |                          |
|   | [ |   |                       |           |   |                          |
|   | 0 |   |                       |           |   |                          |
|   | - |   |                       |           |   |                          |
|   | 5 |   |                       |           |   |                          |
|   | \ |   |                       |           |   |                          |
|   | ] |   |                       |           |   |                          |
|   | \ |   |                       |           |   |                          |
|   | [ |   |                       |           |   |                          |
|   | 0 |   |                       |           |   |                          |
|   | - |   |                       |           |   |                          |
|   | 9 |   |                       |           |   |                          |
|   | \ |   |                       |           |   |                          |
|   | ] |   |                       |           |   |                          |
|   | : |   |                       |           |   |                          |
|   | \ |   |                       |           |   |                          |
|   | [ |   |                       |           |   |                          |
|   | 0 |   |                       |           |   |                          |
|   | - |   |                       |           |   |                          |
|   | 5 |   |                       |           |   |                          |
|   | \ |   |                       |           |   |                          |
|   | ] |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | \ |   |                       |           |   |                          |
|   | [ |   |                       |           |   |                          |
|   | 0 |   |                       |           |   |                          |
|   | - |   |                       |           |   |                          |
|   | 9 |   |                       |           |   |                          |
|   | \ |   |                       |           |   |                          |
|   | ] |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | \ |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | v |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | r |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | k |   |                       |           |   |                          |
|   | 7 |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | / |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | y |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | g |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+
| ! | > |   |                       |           |   |                          |
| [ |   |   |                       |           |   |                          |
| ] | Y |   |                       |           |   |                          |
| ( | o |   |                       |           |   |                          |
| . | u |   |                       |           |   |                          |
| / | > |   |                       |           |   |                          |
| m |   |   |                       |           |   |                          |
| e | h |   |                       |           |   |                          |
| d | a |   |                       |           |   |                          |
| i | v |   |                       |           |   |                          |
| a | e |   |                       |           |   |                          |
| / | > |   |                       |           |   |                          |
| i |   |   |                       |           |   |                          |
| m | n |   |                       |           |   |                          |
| a | o |   |                       |           |   |                          |
| g | w |   |                       |           |   |                          |
| e | > |   |                       |           |   |                          |
| 1 |   |   |                       |           |   |                          |
| 3 | s |   |                       |           |   |                          |
| . | u |   |                       |           |   |                          |
| p | c |   |                       |           |   |                          |
| n | c |   |                       |           |   |                          |
| g | e |   |                       |           |   |                          |
| ) | s |   |                       |           |   |                          |
| { | s |   |                       |           |   |                          |
| w | f |   |                       |           |   |                          |
| i | u |   |                       |           |   |                          |
| d | l |   |                       |           |   |                          |
| t | l |   |                       |           |   |                          |
| h | y |   |                       |           |   |                          |
| = | > |   |                       |           |   |                          |
| " |   |   |                       |           |   |                          |
| 0 | s |   |                       |           |   |                          |
| . | e |   |                       |           |   |                          |
| 2 | a |   |                       |           |   |                          |
| 1 | r |   |                       |           |   |                          |
| 9 | c |   |                       |           |   |                          |
| 4 | h |   |                       |           |   |                          |
| 4 | e |   |                       |           |   |                          |
| 4 | d |   |                       |           |   |                          |
| 4 | > |   |                       |           |   |                          |
| 4 |   |   |                       |           |   |                          |
| 4 | f |   |                       |           |   |                          |
| 4 | i |   |                       |           |   |                          |
| 4 | l |   |                       |           |   |                          |
| 4 | e |   |                       |           |   |                          |
| 4 | s |   |                       |           |   |                          |
| 4 | > |   |                       |           |   |                          |
| 4 |   |   |                       |           |   |                          |
| 4 | u |   |                       |           |   |                          |
| 4 | s |   |                       |           |   |                          |
| i | i |   |                       |           |   |                          |
| n | n |   |                       |           |   |                          |
| " | g |   |                       |           |   |                          |
| h | > |   |                       |           |   |                          |
| e |   |   |                       |           |   |                          |
| i | g |   |                       |           |   |                          |
| g | r |   |                       |           |   |                          |
| h | e |   |                       |           |   |                          |
| t | p |   |                       |           |   |                          |
| = | > |   |                       |           |   |                          |
| " |   |   |                       |           |   |                          |
| 0 | a |   |                       |           |   |                          |
| . | n |   |                       |           |   |                          |
| 2 | d |   |                       |           |   |                          |
| 1 | > |   |                       |           |   |                          |
| 9 |   |   |                       |           |   |                          |
| 4 | s |   |                       |           |   |                          |
| 4 | a |   |                       |           |   |                          |
| 4 | v |   |                       |           |   |                          |
| 4 | e |   |                       |           |   |                          |
| 4 | d |   |                       |           |   |                          |
| 4 | > |   |                       |           |   |                          |
| 4 |   |   |                       |           |   |                          |
| 4 | s |   |                       |           |   |                          |
| 4 | e |   |                       |           |   |                          |
| 4 | a |   |                       |           |   |                          |
| 4 | r |   |                       |           |   |                          |
| 4 | c |   |                       |           |   |                          |
| 4 | h |   |                       |           |   |                          |
| 4 | > |   |                       |           |   |                          |
| i |   |   |                       |           |   |                          |
| n | r |   |                       |           |   |                          |
| " | e |   |                       |           |   |                          |
| } | s |   |                       |           |   |                          |
|   | u |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | s |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | t |   |                       |           |   |                          |
|   | o |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | a |   |                       |           |   |                          |
|   | > |   |                       |           |   |                          |
|   |   |   |                       |           |   |                          |
|   | f |   |                       |           |   |                          |
|   | i |   |                       |           |   |                          |
|   | l |   |                       |           |   |                          |
|   | e |   |                       |           |   |                          |
|   | . |   |                       |           |   |                          |
+---+---+---+-----------------------+-----------+---+--------------------------+

## Review 

> You have now successfully:

1.  Created, copied, moved, and renamed files

2.  Managed file and folder permissions

3.  Made edits to files using text editor vi

4.  Searched through files using text editor vi

5.  Searched through system files using various grep commands

# Lab 8: Cryptography 

## Objectives 

> Upon successful completion of this lab, you will be able to:

1.  Analyze and locate the Certificate Authority (CA) of a website using
    the Windows Certificate Store

2.  Generate a Certificate Signing Request (CSR)

## Task 8.1: Analyze and locate the CA of a website 

> A specific internal website is not correctly loading as it presents
> users with a certificate warning. This issue needs to be resolved
> permanently as the management team is complaining about the nuisance
> of getting the red warning. To help you understand you have also been
> asked to validate some detail regarding sophos.com the certificate and
> issuers.

+---+------------------------------------------+------------------------+
|   | ![](./media/i                            |                        |
|   | mage15.png){width="0.5895833333333333in" |                        |
|   | height="0.5895833333333333in"}           |                        |
|   |                                          |                        |
|   | On **London Client**                     |                        |
+===+==========================================+========================+
| > | > Open **Google Chrome** and navigate to |                        |
|   | > [[https://mail.internet.www]{          |                        |
| 1 | .underline}](https://mail.internet.www/) |                        |
+---+------------------------------------------+------------------------+
| > | > Note down the error being received and |                        |
|   | > hit Proceed:                           |                        |
| 2 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the reason for the          |                        |
|   | > certificate warning and how this error |                        |
| 3 | > can be resolved:                       |                        |
+---+------------------------------------------+------------------------+
| > | > Write down the signature algorithm,    |                        |
|   | > expiration date and how many bits were |                        |
| 4 | > used for the signing CA of             |                        |
|   | > '\*.internet.www':                     |                        |
|   | >                                        |                        |
|   | > Signature algorithm: sha256RSA         |                        |
|   | >                                        |                        |
|   | > RSA 2048bits                           |                        |
|   | >                                        |                        |
|   | > Validity: Wednesday, 5-10-2022         |                        |
+---+------------------------------------------+------------------------+
| > | > Press the Windows key + R to launch    |                        |
|   | > Run                                    |                        |
| 5 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Type **mmc** to launch the Microsoft   | > .                    |
|   | > Management Console                     |                        |
| 6 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Select 'File' on the top menu and      | > This specific        |
|   | > select 'Add or Remove Snap-ins'.       | > snap-in provides a   |
| 7 | > Select **Certificates and click Add    | > list of all the      |
|   | > \>** **Computer Account** \> **Local   | > trusted Cas your     |
|   | > Computer**                             | > computer trusts.     |
|   |                                          | > Browsers such as     |
|   |                                          | > Google Chrome and    |
|   |                                          | > Internet             |
|   |                                          | >                      |
|   |                                          | > Explorer utilize     |
|   |                                          | > your systems         |
|   |                                          | > certificate store    |
+---+------------------------------------------+------------------------+
| > | > Make the necessary changes in the      |                        |
|   | > Certificate snap-in to resolve the     |                        |
| 8 | > certificate warning and restart Google |                        |
|   | > Chrome to apply these changes          |                        |
+---+------------------------------------------+------------------------+
| > | > Open **sophos.com in Google Chrome**   |                        |
|   | > and read the certificate and all its   |                        |
| 9 | > issuers                                |                        |
+---+------------------------------------------+------------------------+
| > | > Write down why this certificate is     |                        |
|   | > considered trusted and provide any     |                        |
| 7 | > evidence for this reasoning using the  |                        |
|   | > mmc console:                           |                        |
+---+------------------------------------------+------------------------+
| ! | > You have successfully reviewed and     |                        |
| [ | > resolved a website certificate issue.  |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Task 8.2: Generate a CSR using OpenSSL to prepare a certificate 

> You have been tasked with creating a new certificate using the
> Company's CA. The certificate being created will be used in a future
> deployment of a webserver. The private key needs to be saved and be
> password protected.

+---+------------------------------------------+------------------------+
|   | ![](./media/i                            |                        |
|   | mage14.png){width="0.5847222222222223in" |                        |
|   | height="0.5847222222222223in"}           |                        |
|   |                                          |                        |
|   | On **London DC**                         |                        |
+===+==========================================+========================+
| > | > Use openssl.exe through windows        | > OpenSSL is in        |
|   | > command prompt to generate a CSR.      | >                      |
| 1 |                                          | > C:                   |
|   |                                          | \\Users\\Administrator |
|   |                                          | \\Downloads\\OpenSSL\\ |
|   |                                          | > bin\\openssl.exe     |
+---+------------------------------------------+------------------------+
| > | > Use the following command with         | > The private key is   |
|   | > openssl.exe to generate a CSR and      | > generated during CSR |
| 2 | > private key pairing. Fill in the       | > creation. Treat this |
|   | > requested fields with the information  | > like you would a     |
|   | > of your choosing:                      | > password.            |
|   | >                                        | >                      |
|   | > req -new -newkey rsa:4096 -nodes       | > Take note of the     |
|   | > -keyout private.key -out               | > .csr and .key        |
|   | > certificate.csr                        | > location for future  |
|   |                                          | > use.                 |
+---+------------------------------------------+------------------------+
| > | > Open Google Chrome and navigate to     | > We are accessing a   |
|   | > [<                                     | > Certificate          |
| 3 | https://localhost/>certsrv/]{.underline} | > Authority to         |
|   |                                          | > generate a           |
|   |                                          | > certificate.         |
+---+------------------------------------------+------------------------+
| > | > Hit Submit and take note of the        |                        |
|   | > Request ID:                            |                        |
| 4 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Go to 'Advanced certificate request'   |                        |
|   | > and copy/paste the contents of the     |                        |
| 5 | > .csr.                                  |                        |
+---+------------------------------------------+------------------------+
| > | > Open Windows 'Certification Authority' |                        |
|   | > from the administrative tools and find |                        |
| 6 | > the newly requested certificate under  |                        |
|   | > 'Pending Requests'.                    |                        |
+---+------------------------------------------+------------------------+
| > | > Select the certificate and right click | > We are accepting the |
|   | > and select **All Tasks \> Issue**      | > certificate signing  |
| 7 |                                          | > request.             |
+---+------------------------------------------+------------------------+
| > | > Under Issued Certificates, find the    |                        |
|   | > new certificate                        |                        |
| 8 |                                          |                        |
+---+------------------------------------------+------------------------+
| > | > Right click the certificate and select |                        |
|   | > **Open** to analyze the newly          |                        |
| 9 | > generated certificate details          |                        |
+---+------------------------------------------+------------------------+
| > | > Write down why the private key was not |                        |
|   | > required by the CA signer:             |                        |
| 1 |                                          |                        |
| 0 |                                          |                        |
+---+------------------------------------------+------------------------+
| 1 | > Write down where the information in    |                        |
| 1 | > the newly generated certificate came   |                        |
|   | > from:                                  |                        |
+---+------------------------------------------+------------------------+
| > | > Who is the issuer of the certificate?  |                        |
|   | >                                        |                        |
| 1 | > How was the issuer decided?            |                        |
| 2 |                                          |                        |
+---+------------------------------------------+------------------------+
| ! | > You have now successfully created a    |                        |
| [ | > CSR and certificate pair               |                        |
| ] |                                          |                        |
| ( |                                          |                        |
| . |                                          |                        |
| / |                                          |                        |
| m |                                          |                        |
| e |                                          |                        |
| d |                                          |                        |
| i |                                          |                        |
| a |                                          |                        |
| / |                                          |                        |
| i |                                          |                        |
| m |                                          |                        |
| a |                                          |                        |
| g |                                          |                        |
| e |                                          |                        |
| 1 |                                          |                        |
| 3 |                                          |                        |
| . |                                          |                        |
| p |                                          |                        |
| n |                                          |                        |
| g |                                          |                        |
| ) |                                          |                        |
| { |                                          |                        |
| w |                                          |                        |
| i |                                          |                        |
| d |                                          |                        |
| t |                                          |                        |
| h |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| h |                                          |                        |
| e |                                          |                        |
| i |                                          |                        |
| g |                                          |                        |
| h |                                          |                        |
| t |                                          |                        |
| = |                                          |                        |
| " |                                          |                        |
| 0 |                                          |                        |
| . |                                          |                        |
| 2 |                                          |                        |
| 1 |                                          |                        |
| 9 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| 4 |                                          |                        |
| i |                                          |                        |
| n |                                          |                        |
| " |                                          |                        |
| } |                                          |                        |
+---+------------------------------------------+------------------------+

## Review 

> You have now successfully:
>
> 1\. Analyzed and located the Certificate Authority (CA) of a website
> using the Windows Certificate Store 2. Generated a Certificate Signing
> Request (CSR)

![](./media/image17.jpg){width="8.256944444444445in"
height="11.65in"}![](./media/image18.png){width="3.7777777777777777in"
height="1.2284722222222222in"}
