# **Lab 3: Active Directory**

## Objectives
Upon successful completion of this lab, you will be able to: 
1.	Create OUs, groups, and users in Active Directory 
2.	Modify and identify both user and group attributes 



### Lab Diagram:
![London DC](JPG/London%20DC%202.png)

***

## **Task 3.1:** OU, Group and User Configuration 

You have been assigned a task to setup a user, group and an OU in Active Directory: 
  
![](JPG/London%20DC%204.png)
1. Create three OUs with the following names: UK, Canada, and India 
> Create these OUs under `SOPHOS.LOCAL`

2. Create three sub-OUs with the following names:
  
| OU | Sub-OU   |
|----|----------|
| UK | Abingdon |
|Canada| Vancouver |
| India | Ahmedabad |

 3. Create two users in each sub-OU:
 
| OU |	User  |
|----|--------|
| Abingdon | UserA, UserB |
| Vancouver |	UserC, UserD |
| Ahmedabad |	UserE, UserF |


4. Create the user group ‘Sales’ in the Abingdon OU and add UserA to it
5. Create the user group, ‘Finance’ in the India OU and add UserF to it



##### ![check](JPG/pngegg%20(1).png) You have created OUs, Users, and Groups in Active Directory

***

## **Task 3.2:** <small>User and Group Attribute Troubleshooting</small> 
You have been asked to troubleshoot the following task in Active Directory

![](JPG/London%20DC%204.png)  
1. List the distinguished name for **‘UserA’** and **‘UserD’**:
2. Write down the **Mail**, **UserPrincipalName** and the **sAMAccountName** attribute for user ‘**Jane Doe**’:
3. Write down the displayName, GroupID and **Common Name** for user ‘**Lucy Fox**’:
4. Write down the **objectGUID** and **Distinguished name** for group ‘**Sales**’:


##### ![check](JPG/pngegg%20(1).png) You have successfully verified user and group attributes 

***


## ![review](JPG/Review%2048.png) Review  ##

You have now successfully: 
* Created OUs, groups, and users in Active Directory 
* Modified and identified both user and group attributes 




