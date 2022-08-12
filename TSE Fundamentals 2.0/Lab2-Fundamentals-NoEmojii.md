# **Lab 2: Windows Server**

## Objectives
Upon successful completion of this lab, you will be able to: 
1.	Review roles installed on a Windows Server 
2.	Apply password complexity requirements using Group Policies 


### Lab Diagram:
![London DC](JPG/London%20DC%202.png)

***

## **Task 2.1** Group Policies
You have recently been given access to the Domain Controller. Your task is to force all users to set a password with a minimum length of 10.   

![](JPG/London%20DC%204.png)
1. Open Server Manager and select **Manage > Add Roles and Features**  

2. Read the **‘Before you begin’** message and click **Next** 

3. Keep **‘Role-based or feature-based installation’** selected and click **Next** twice  

4. Note down the server roles installed on this server.  

5. Click **Cancel** to exit out of Add Roles and Features 

6. Open **Group Policy Management** 

7. Navigate to Forest: `SOPHOS.LOCAL > Domains > SOPHOS.LOCAL`

8. Right-click `SOPHOS.LOCAL` and select:   
**Create a GPO in this domain and link it here…**  

9. In the **‘Name’** field enter **"Password policy"** then hit **OK**   
 
10. Right-click Password policy and select **Edit…**  

11. in the left-hand panel, select:  
 `Computer Configuration > Windows Settings > Security Settings > Account Policies > Password Policy`

12. Double click **"Minimum password length"**

13. Select Define this policy and set the **password length** to **10 characters**

14. Click **OK**

##### ![check](JPG/pngegg%20(1).png) You have successfully noted down the installed features on a server and created a group policy

***

## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
* Reviewed roles installed on a Windows Server
* Applied password complexity requirements using Group Policies



***




