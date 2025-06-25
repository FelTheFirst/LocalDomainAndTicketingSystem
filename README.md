# LocalDomainAndTicketingSystem

This is a walkthrough of a home lab in which I created a rudimentary local domain. I chose to mimic the business structure of a resort. I believed this choice would be beneficial to exploring a business with many departments and various roles in those departments.


## Tools Used:

Oracle VirtualBox -As the virtualization platform to host the lab

Windows Server 2019 ISO -As the OS of choice to mimic enterprise environments

Spiceworks -As the ticketing system 


## Initial Lab Set Up

I began with downloading Oracle VirtualBox and the Windows Server 2019 ISO from their official websites. 

Then I installed the ISO on to the VM and began patch management on the OS.

After all the system and security patches were up to date, I upgraded guest additions in the lab. This downloaded certain drivers like the mouse integration driver, and allowed me to optimize my lab environment.

Next, I set a static IP for the server through the network adapter setting in the Windows server. I set a private IP address and directed the server to use itself as the DNS server.

Then I moved on to Active Directory and Domain Services (AD DS) setup. I installed AD DS and promoted the server to domain controller.

I named the new domain "resort.local" to reflect the simulated business environment. 

## Departments, Users, and Groups

With the lab environment and domain established I moved on to the core of the project. I created Organizational Units (OUs) for each resort department. These included:

- IT 
- Support
- Accounting
- Customer Service (with subgroups for Concierge, and Front Desk)
- Food and Beverage
- Retail
- Housekeeping

Inside each OU I created two user accounts to simulate a functioning workplace.

I also created:

- IT Admins and Service Desk security groups to simulate different access levels within the IT department
- Custom security groups for Concierge and Front Desk roles within customer service

This structure allowed me to practice:

- Creating users and groups in active directory
- Organizing users using OUs
- Planning a logical permissions to establish a Role Based Access Control (RBAC) approach for the resort

## Folder Permissions

To simulate real world access controls, I created department specific folders on the server and used Microsoft's New Technology File System (NTFS) permissions to control access.

Each department's folders were configured so that:
  
  - Only members of that department or roles security group could read/write inside their own folder
  - Users outside of that specific department/role were denied access to the folder
  - IT Admins had full access to all departments folders for, the Support team had the same access except they did not have access to IT Admins folder

This gave me hands-on experience managing permissions:

  - Security Groups
  - Access Controls Lists (ACLs)
  - RBAC Principles

## Help Desk Simulation with Spiceworks

After I established the environment, I wanted to simulate IT support workflows. So, I set up a Spiceworks account and used their lightweight browser-based ticketing system to mimic a ticketing system that might be found in and enterprise environment.

I used Spiceworks to:

 - Create and respond to simulated support tickets. (Password Resets, Access Requests, Printer Issues)
 - Document issues and track resolution steps
 - Assign tickets based on department or urgency

This portion of the lab helped me experience a basic IT ticketing system and reinforced the following:

 - My understanding of the ticket lifecycle
 - The importance of documentation
 - The importance of clear communication with the end user
 - Ticket classification and prioritization

# Project Reflection
With this project I wanted to revisit some of the fundamental skills I developed earlier on in my studies. The CompTIA A+ was the first technical certificate I ever achieved, and while I know I am comfortable with the theoretical knowledge
I gained during my time studying for that. I did not want to lose the practical skills I gained as I continue to dive deeper into topics like security and cloud computing. I believe it's important to revisit the fundamentals every so often, and to showcase
that beyond holding a certificate, I can actually do the work. I proudly call myself a continuous learner, but that doesn't always mean learning the next newest thing. It also means going out of my way to gain more solid hands-on experience with topics I have already covered.

I am glad I took the time to complete this home lab, as it gave me the opportunity to gain practical experience with the following:

 - Setting up and managing a Windows Server 2019 Domain
 - Creating users, groups and OUs in Active Directory
 - Configuring Static IPs and understanding the role of DNS in domain environments
 - Implementing NTFS permissions and RBAC
 - Simulating real world IT support workflows using a help desk ticketing system

This project helped me connect all the pieces of my studies into a real-world setting. It helped me gain a better understanding of enterprise IT support work as a whole, and helped me gain confidence in a Windows server. 

Thank you for taking the time to read through my project. 

Have a great day
-Fel

 
  
  
