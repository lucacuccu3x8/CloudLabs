# **Lab 2: Windows Server**

## Objectives
Upon successful completion of this lab, you will be able to: 
1. Review roles installed on a Windows Server
2. Apply password complexity requirements using Group Policies 


### Lab Diagram:
![London DC](JPG/London%20DC%202.png)

***

## **Task 2.1** Review Roles
You have recently been given access to the Domain Controller. Your task is disable Control Panel for users.

![](JPG/London%20DC%204.png)
1. Open **Server Manager** and select **Manage > Add Roles and Features**  

2. Read the **‘Before you begin’** message and click **Next** 

3. Keep **‘Role-based or feature-based installation’** selected and click **Next** twice  

4. Note down the server roles installed on this server.   
> You want to make sure that "Active Directory Domain Service" role is active.

5. Click **Cancel** to exit out of Add Roles and Features 


----
## **Task 2.2** Modify Group Policies

6. From the same **Server Manager**, navigate in **Tools** and open **Group Policy Management** 



7. Navigate into the Forest: `SOPHOS.LOCAL > Domains > SOPHOS.LOCAL`

8. Right-click `SOPHOS.LOCAL` and select:   
**Create a GPO in this domain and link it here…**  
![](JPG/GroupPolicy1.jpg)

9. In the **‘Name’** field enter **"Password policy"** then hit **OK**   


 
10. Right-click Password policy and select **Edit…**  
![](JPG/GroupPolicy2.jpg)


11. in the left-hand panel, select: 
`User Configuration > Policies > Administrative Templates > Control Panel`

12. Double click **"Prohibit access to Control Panel and PC settings"**
![](JPG/2.1.12B.png)

13. Set the policy to **"Enabled"** and Click **OK**

14. Login in the London Client as:
* User: `SOPHOS\jsmith`
* Password: `Sophos1985`

![](JPG/London%20Client.png)


15. Open the **PowerShell** with elevated permissions and invoke the following command:
```powershell
gpupdate /force
```

16. Click on windows John Smith and Sign out

17. To test the new settings, log off and log back as Jsmith

18. Try opening Control Panel. The policy will prevent access of the Control Panel with the following pop-up: 

![](JPG/popup.png)

19.	Close the warning pop-up and log out the current user.

20.	Switch to London DC

21.	Open **Group Policy Management** console.

22.	Right-Click on **Control Panel Policy** and click **Link Enabled**. This will disable the GPO Link and hence won’t apply the GPO settings anymore.

23.	Close **Group Policy Management** console and all the other open windows.

24.	see more information about the PowerShell command here: https://activedirectorypro.com/gpupdate-command/


### ![check](JPG/pngegg%20(1).png) You have successfully noted down the installed features on a server and created a group policy

***

## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
*	Reviewed roles installed on a Windows Server
*	Disable control panel settings using Group Policies
*	Applying the GPO’s and testing the results.




***
***
### Before closing this page:
> Please remember to "Deallocate" the "HostVM" in the "Resource Tab" before closing this LAB, 
![](JPG/Deallocate%20the%20VM.png)
otherwise please continue to the next LAB.



