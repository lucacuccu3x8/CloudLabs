# **Lab 2: Windows Server**

## Objectives
Upon successful completion of this lab, you will be able to: 
1. Review roles installed on a Windows Server
2. Apply administrative settings using Group Policies 
3. Applying the GPO’s and testing the results


### Lab Diagram:
![London DC](JPG/London%20DC%202.png)

***


## **Task 2.1** Review Roles
Review the roles and features already installed on a Windows Server which is a Domain Controller.

![](JPG/London%20DC%204.png)

Logon on London-DC using the following:

Username: **administrator**

Password: **Sophos1985**
1. To open Server Manager, click the **Server Manager** icon in the taskbar or select **Server Manager** in the Start Menu. 

2. In the Dashboard, you can see the list of the Roles installed under **Roles and Server Group**
> Make a note of the number of installed roles: 

3. Click Manage in the upper right portion of the screen and click **Add Roles and Features** to open a wizard.  

4. On the Select installation type page, choose **Role-based or feature-based installation** and click Next  twice.   

5. On the Select server role you can see a list of roles installed on the Server. 
Make a note of the installed roles on this server.
> Note: You want to ensure that the "Active Directory Domain Service" role is active.

6. Click next, and you’ll see a list of features installed on this server. Scroll down to have a look at the features.

7. Click Cancel to exit out of Add Roles and Features Wizard.

8. Close all open Windows.




----
## **Task 2.2** Create and Modify Group Policy
In this task, you'll see how to apply Group Policy Objects at the domain and verify how the settings are applied.
1. Open Group Policy Management by navigating to the **Start menu** > **Server Manager**> **Tools**, then select **Group Policy Management**.

2. In the navigation pane, expand Forest:**SOPHOS.LOCAL**, expand **Domains**, expand **SOPHOS.LOCAL**, and then click **Group Policy Objects**
> Note: This will show the list of GPOs in the current domain.

3. Right-click **SOPHOS.LOCAL** and select **Create a GPO in this domain and link it here**  
![](JPG/GroupPolicy1.jpg)

4. In the ‘Name’ field enter **"Control Panel Policy"** then hit **OK**   
![](JPG/Control%20Panel%20Policy.jpg)

 
5. Right-click **"Control Panel Policy"** and select **Edit…**  
![](JPG/Control%20Panel%20Policy%202.jpg)


6. In the left-hand panel, select: `User Configuration > Policies > Administrative Templates > Control Panel`
![](JPG/Control%20Panel%20Policy%203.jpg)

7. Double click **"Prohibit access to Control Panel and PC settings"**
![](JPG/2.1.12B.png)

8. Set the policy to **"Enabled"** and Click **OK**

9. Minimize all open windows 

### ![check](JPG/pngegg%20(1).png) You have successfully created the Group Policy Object and modified the settings. 

***
## **Task 2.3** Applying and Testing Group Policies
In this task we will apply the Group policy and testing if the settings are applied.
![](JPG/London%20Client.png)

Switch to the London Client and log in as: 
> User: `SOPHOS\jsmith`
> Password: `Sophos1985`


1. Open the **PowerShell** with elevated permissions and invoke the following command:
```powershell
gpupdate /force
```

2. Click on windows John Smith and Sign out

3. To test the new settings, log off and log back as Jsmith

4. Try opening Control Panel. The policy will prevent access of the Control Panel with the following pop-up: 

![](JPG/popup.png)

5.	Close the warning pop-up and log out the current user.

6.	Switch to London DC

7.	Open **Group Policy Management** console.

8.	Now let's disable the same policy by Right-Click on **Control Panel Policy** untick **Link Enabled**. This will disable the GPO Link and hence won’t apply the GPO settings anymore. 

![](JPG/untick.jpg)

9.	Close **Group Policy Management** console and all the other open windows.

> Note for more information about the PowerShell command here: https://activedirectorypro.com/gpupdate-command/


### ![check](JPG/pngegg%20(1).png) You have successfully tested the Group Policy settings on the Windows Endpoint.

***

## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
*	Reviewed roles installed on a Windows Server
*	Disable control panel settings using Group Policies
*	Applying the GPO’s and testing the results

# **Lab 2.1: Active Directory**

## Objectives
Upon successful completion of this lab, you will be able to: 
1.	Create OUs, groups, and users in Active Directory 
2.	Modify and identify both user and group attributes 

***

### Lab Diagram:
![London DC](JPG/London%20DC%202.png)

***

## **Task 2.1.1:** OU, Group and User Configuration 

You have been assigned a task to create **Users**, **Groups** and an **OU's** in Active Directory: 
  
![](JPG/London%20DC%204.png)
Logon on London-DC using the following:

Username: **administrator**

Password: **Sophos1985**

1. From the **Server Manager > open the **Active Directory Users and Computers** console

2. Right-click `SOPHOS.LOCAL`, and select **New** > **Organizational Unit** with following names ( create all three Ou's):
>* `UK` 
>* `Canada`
>* `India`
![](JPG/Active%20directory%20Users%20and%20Groups.png)
 
 


3. Using the same steps above, under the previously created **OUs**, create three new **sub-OUs** with the following names:
  
| OU | Sub-OU   |
|----|----------|
| UK | `Abingdon` |
|Canada| `Vancouver` |
| India | `Ahmedabad` |

4. Now, create two **users** in each **sub-OU**:
 
| OU |	User  |
|----|--------|
| Abingdon | `UserA`, `UserB` |
| Vancouver |	`UserC`, `UserD` |
| Ahmedabad |	`UserE`, `UserF` |
> **Note:** leave the password field empty and press **Finish** to create the user
![](JPG/New%20User2.png)

5. Create the Group "**Sales-UK**" in the "**Abingdon OU**" 

6. Right-click "**UserA**" and select **"Add to a group..."**    
Type `Sales-UK` in the search box and confirm with **"Check Names"**

7. Press **OK** twice; a confirm prompt should appear:
![](JPG/confirm.png)

8. Use the same steps above to create another Group "**Finance**" in the "**Ahmedabad OU**" and add "**UserF**" to it.

9. Leave the "**Active Directory Users and Computers**" console open for the next Task.



#### ![check](JPG/pngegg%20(1).png) You have successfully created OUs, Users, and Groups in Active Directory

***

## **Task 2.1.2:** <small>Verify attributes of Active Directory Objects</small> 
In this task, you will be verifying the attributes of Active Directory Objects.

![](JPG/London%20DC%204.png)  
1. List the **distinguished name** for **‘UserA’** and **‘UserD’**.

***
#### ![](JPG/Knowledge%203.png) How to find the **"distinguishedName"** of an **OU**:

> a) In the "**Active Directory Users and Computers**" console, select **View > Advanced Features**.
![](JPG/Advanced%20View.png)
> b) Click on  the Abingdon OU, **Right-Click** the UserA and then select **Properties**.
> c) In the Properties, select the **Attribute Editor** tab.   
> d) Click on **distinguishedName** to highlight it, then click **View**
> Example: ![](JPG/Attreibutes.png)
***

2. Write down the **Mail**, **UserPrincipalName** and the **sAMAccountName** attribute for user ‘**Jane Doe**’:
3. Write down the displayName, GroupID and **Common Name** for user ‘**Lucy Fox**’
4. Write down the **objectGUID** and **Distinguished name** for group ‘**Sales**’
5. You can now close down the **"Active Directory users and Computers"**


##### ![check](JPG/pngegg%20(1).png) You have successfully verified user and group attributes 

***


## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
* Created OUs, groups, and users in Active Directory 
* Modified and identified both user and group attributes 

***
***
### Before closing this page:
> Please remember to "Deallocate" the "HostVM" in the "Resource Tab" before closing this LAB, 
![](JPG/Deallocate%20the%20VM.png)
otherwise please continue to the next LAB.





