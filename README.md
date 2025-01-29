<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Users and Computers Microsoft Azure</h1>
This tutorial outlines the implementation of creating users and computers in Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>


- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Searching for objects in Active Directory
- Groups and Memberships
- Creating Users
- Resetting passwords
- Disabling and deleting Users
- Configure Users, OUs.


<h2>Deployment and Configuration Steps</h2>




<p>
STEP 1 : The initial step in configuring Active Directory involves accessing the domain controller and navigating to the Active Directory Users and Computers (ADUC) console through the Server Manager's Tools menu. This critical process enables administrators to create a new Organizational Unit (OU) within the domain structure, providing a foundational element for efficient user management and policy application. By strategically designing and implementing OUs, IT professionals can establish a hierarchical framework that aligns with the organization's structure, facilitating streamlined administration, enhanced security through granular permissions, and the ability to apply targeted Group Policy Objects (GPOs) to specific segments of the network environment.
</p>
<p>
<img width="1512" alt="Screenshot 2025-01-27 at 11 29 57 AM" src="https://github.com/user-attachments/assets/689df4a5-bcff-4cea-b379-5997cee0cf9f" />

<img width="1512" alt="Screenshot 2025-01-27 at 11 33 17 AM" src="https://github.com/user-attachments/assets/dcbf6b5e-6e55-4e72-94ee-3a81132a4a97" />

</p>
<br />


<p>
STEP 2 : In the next phase of Active Directory configuration, create two additional Organizational Units (OUs) within the domain folder: one for "Computers" and another for "Users". This strategic segregation aligns with industry best practices, enabling more efficient management of user accounts and computer objects by providing a clear, logical structure within the Active Directory hierarchy. By implementing this organizational approach, administrators can apply targeted Group Policies, streamline security measures, and facilitate easier troubleshooting and auditing processes, ultimately enhancing the overall manageability and security posture of the network environment.
</p>
<p>
<img width="1512" alt="Screenshot 2025-01-27 at 11 44 16 AM" src="https://github.com/user-attachments/assets/aa618c95-2a94-40b4-b534-a3ec140d5e39" />



</p>
<br />




<p>
Step 3 To create a new user account, right-click on the "Domain Users" OU and select "New" > "User" from the context menu, following the visual guidance provided in the accompanying image. Adhere to the best practice of using the format "firstname.lastname" for the user's login name, ensuring consistency and ease of identification across the domain. When configuring the account, be sure to uncheck the "User must change password at next logon" option to prevent potential authentication issues, particularly for users connecting via VPN, thus streamlining the initial login process and reducing potential support tickets.
</p>
<p>
<img width="1512" alt="Screenshot 2025-01-27 at 11 54 42 AM" src="https://github.com/user-attachments/assets/a8bea3a4-431f-4dc1-b8f1-cd08b4b9c64d" />

<img width="1512" alt="Screenshot 2025-01-27 at 11 56 34 AM" src="https://github.com/user-attachments/assets/25d0f0d0-ea78-450f-be0f-5d07260c60a0" />

<img width="1512" alt="Screenshot 2025-01-27 at 11 59 58 AM" src="https://github.com/user-attachments/assets/a93b256d-fb7f-4dc9-a0dc-1173bee5a943" />


</p>
<br />



<p>
In Step 4 : Upon receiving a call from John regarding password recognition issues, navigate to Active Directory Users and Computers to locate his account. Verify John's identity by right-clicking on his name, selecting "Properties," and confirming that the username matches the correct John, as there may be multiple users with the same name in the system. Once verified, right-click on John's account and select "Reset Password" to securely change his credentials, ensuring he regains access to the system while maintaining proper account management protocols.
</p>
<p>
<img width="1512" alt="Screenshot 2025-01-27 at 12 16 49 PM" src="https://github.com/user-attachments/assets/e1afd857-3ec4-4061-bed8-63ba4819304e" />
<img width="1512" alt="Screenshot 2025-01-27 at 12 21 42 PM" src="https://github.com/user-attachments/assets/29394ca2-1e14-4fe0-929f-f17058eb0d5f" />
<img width="1512" alt="Screenshot 2025-01-27 at 12 22 34 PM" src="https://github.com/user-attachments/assets/f961141c-3981-4ac7-806f-b34242405e79" />


</p>
<br />







<p>
To unlock John's account without changing his password, navigate to Active Directory Users and Computers and locate John's user object. Access John's properties by right-clicking his account and selecting "Properties," then switch to the "Account" tab within the properties window. In the "Account options" section, locate and check the box labeled "Unlock account," then click "Apply" and "OK" to confirm the changes, effectively restoring John's ability to log in without altering his existing password.
</p>
<p>

<img width="1512" alt="Screenshot 2025-01-27 at 12 27 14 PM" src="https://github.com/user-attachments/assets/4c771748-3540-4524-a7b6-efec041ca153" />


</p>
<br />




<p>
To create a new security group for sales personnel, navigate to the Domain Users Organizational Unit (OU) in Active Directory Users and Computers, then right-click and select "New" > "Group". In the New Object - Group dialog, name the group "Sales", set the Group scope to "Global" and the Group type to "Security", enabling you to assign permissions and allow members to access resources across trusting domains within the same forest. This configuration establishes a flexible and secure group structure that facilitates efficient management of sales team access rights and resources throughout the organization's Active Directory environment.
</p>
<p>

<img width="1512" alt="Screenshot 2025-01-27 at 1 17 24 PM" src="https://github.com/user-attachments/assets/dbeffa9e-c091-49fb-ac7b-3fcbb8d27984" />



</p>
<br />








<p>
To add the newly created user, John, to the Sales group, right-click on the Sales group in Active Directory Users and Computers and select "Properties" from the context menu. Navigate to the "Members" tab within the Properties window, then click the "Add" button to open the Select Users, Contacts, Computers, or Groups dialog. In this dialog, enter John's username, click "Check Names" to verify, and then click "OK" to confirm, effectively granting John the permissions and access rights associated with the Sales group across the domain.
</p>
<p>
<img width="1512" alt="Screenshot 2025-01-27 at 1 29 27 PM" src="https://github.com/user-attachments/assets/8ddfd33f-3d07-4356-b0be-f86f504af624" />





</p>
<br />




<p>
To verify a user's group memberships, right-click on the user object in Active Directory Users and Computers and select "Properties" from the context menu. Navigate to the "Member Of" tab within the Properties window to view a comprehensive list of groups the user belongs to, including the recently assigned "Sales" group for John Garcia. This method provides a quick and efficient way to confirm group assignments, ensuring that users have the appropriate access rights and permissions within the Active Directory environment.
</p>
<p>

<img width="1512" alt="Screenshot 2025-01-27 at 1 33 36 PM" src="https://github.com/user-attachments/assets/2d01ad88-4aea-42ff-a3de-bf0725d89456" />




</p>
<br />


<p>
To manage users who have left the company or no longer require access, create a new Organizational Unit (OU) named "Inactive Users" within Active Directory Users and Computers. When a user's access needs to be revoked, right-click on their user object in the Users OU, select "Disable Account" from the context menu, and confirm the action. After disabling the account, drag and drop the user object into the "Inactive Users" OU, effectively organizing and segregating these accounts for improved security and management, while maintaining an audit trail of former employees.
</p>
<p>

<img width="1512" alt="Screenshot 2025-01-27 at 2 42 08 PM" src="https://github.com/user-attachments/assets/40cf6d75-4ef5-4e9f-9d3b-dfea98d813e5" />

<img width="1512" alt="Screenshot 2025-01-27 at 2 46 04 PM" src="https://github.com/user-attachments/assets/e24b6f94-40dc-4740-a54d-0faa7c64a1ad" />

<img width="1512" alt="Screenshot 2025-01-27 at 2 47 12 PM" src="https://github.com/user-attachments/assets/29431506-ebdf-429e-bff6-e451990195b8" />


</p>
<br />




















