<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Begin to configure roles, departments, and teams.
- Continue to build out the ticketing system by configuring Agents and Users.
- Configure SLA (Service Level Agreements) for three different severities of tickets.
- Configure help topics for users to put as header when submitting tickets.

<h2>Configuration Steps</h2>

<p>

  ![image](https://github.com/michaelpeters2/post-install-config/assets/141062110/9036390d-3666-45da-8e67-77300e5ba630)

Configure Roles
- From Admin Panel -> Agents -> Roles -> Add New Role
- Name: Supreme Admin
- Grant all permissions for tickets, tasks, and knowledgebase.
</p>
<br />

![image](https://github.com/michaelpeters2/post-install-config/assets/141062110/171c3015-0c3e-48e5-8c12-2d90a2c30f74)

Configure Departments
- From Admin Panel -> Agents -> Departments
- Name: System Administrators
- Leave settings default
</p>
<br />

![image](https://github.com/michaelpeters2/post-install-config/assets/141062110/8c747590-4cf1-4b62-94cd-03f2d4c78a05)

Configure Teams
- From Admin Panel -> Agents -> Teams
- Level I Support (should be pre-made, if not, create it)
- Level II Support

</p>
<br />
From Admin Panel -> Settings -> Users
- Confirm that "Registration Required" is UNCHECKED. This allows anyone to create tickets.
<br />

![image](https://github.com/michaelpeters2/post-install-config/assets/141062110/a9bb4bc4-5dd2-46e9-a9d3-66f8961f92ed)

Configure Agents (workers)
- From Admin Panel -> Agents -> Add New
- Create Jane -> Access -> Department: System Administrator -> Role: Supreme Admin
- From Teams -> Level 2 Support
- Create John -> Access -> Department: Support -> Role: View Only
- Set both passwords as Password1. *Don't Require Change*


![image](https://github.com/michaelpeters2/post-install-config/assets/141062110/43543c64-f2d1-41e3-af3d-2e035a7cb270)


Configure Users (customers)
- From AGENT Panel -> Users -> Add New
- Karen -> Email: Karen@osTicket.com -> Name: Karen Karen
- Ken -> Email: Ken@osticket.com -> Name: Ken Ken

![image](https://github.com/michaelpeters2/post-install-config/assets/141062110/0b689795-9a2f-4163-b8d6-f38ee17a173d)

Configure SLA (Service Level Agreement)
- From Admin Panel -> Manage -> SLA
- Sev-A (1 hour, 24/7)
- Sev-B (4 hours, 24/7)
- Sev-C (8 hours, business hours)

![image](https://github.com/michaelpeters2/post-install-config/assets/141062110/b76e8bdb-0adb-4eec-9fb4-cbdf528d945a)


Configure Help Topics
- From Admin Panel -> Manage -> Help Topics
- Business Critical Outage
- Personal Computer Issues
- Equipment Request
- Password Reset
