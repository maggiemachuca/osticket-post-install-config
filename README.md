<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure a role of **Full Admin** to assign full administrative access to agents who need this role.
- Configure the department of **System Administrators**
- Configure the team of **Online Banking**
- Allow end users to create trouble tickets
- Configure agents (employees) so that we can assign them to a department
- Configure agents' passwords
- Configure end user accounts (customers)
- Configure our 3 **Service Level Agreements**
- Configure **help topics** so that our end users can specify their issue(s)

<h2>Configuration Steps</h2>

## Step 1: Configure Roles

- We are going to be using this link to log into our <a href="http://localhost/osTicket/scp/login.php">admin page</a>
- Open this link inside of the machine you configured osTicket on
- Enter the admin credentials

<img width="477" height="383" alt="Screenshot 2025-09-22 at 3 20 22 PM" src="https://github.com/user-attachments/assets/63103fc0-f314-4d2b-9073-9066f4501985" />

- Click **Admin Panel** (screenshot below)

<img width="993" height="390" alt="Screenshot 2025-09-22 at 3 24 58 PM" src="https://github.com/user-attachments/assets/5fd042eb-fb70-4672-b3dd-e4140cab53ba" />

- Click the **Agents** tab
- Click the **Roles** tab

<img width="962" height="341" alt="Screenshot 2025-09-22 at 3 29 11 PM" src="https://github.com/user-attachments/assets/ddc52a4e-a3fb-4251-bc95-8e380520765e" />

- We are going to be making a role that has **full admininstrative access**
- Click **Add new role**
- Type the name you want for this admin role, it will have permissions to do everything
- Click **Permissions**

<img width="961" height="385" alt="Screenshot 2025-09-22 at 3 32 19 PM" src="https://github.com/user-attachments/assets/768a69ef-fa42-4b70-8b04-12fdd4492ffd" />

- In this tab you will see a list of permissions you can assign
- For the full admin role we will be putting a checkmark on everything
- The **Tickets**, **Tasks**, **Knowledgebase** tabs should have a checkmark on everything too
  
<img width="536" height="490" alt="Screenshot 2025-09-22 at 3 47 05 PM" src="https://github.com/user-attachments/assets/5dcf8326-50c4-45fc-965b-6adc179ca7f8" />

- Click **Add role** when you are done

<img width="89" height="36" alt="Screenshot 2025-09-22 at 3 48 27 PM" src="https://github.com/user-attachments/assets/a21edc98-5424-4550-80e8-46fa0fe1f296" />

- Your screen should tell you that you were successful
  
<img width="205" height="40" alt="Screenshot 2025-09-22 at 3 49 13 PM" src="https://github.com/user-attachments/assets/34510da5-9263-41de-8eed-e70b5063cf46" />

## Step 2: Configure Departments
<p>In this step we are going to add the role of System Administrator</p>

- Next we are going to configure our departments
- Since we are already in the Admin Panel, go ahead and click **Departments**

<img width="961" height="427" alt="Screenshot 2025-09-22 at 3 50 32 PM" src="https://github.com/user-attachments/assets/28bc2cfd-c1a8-4791-8206-f33969524d99" />

- Click **Add New Department**
- For the Parent, select **Top-Level-Department** (see screenshot below)
- Name your role **SysAdmins**
- Click **Create Dept**

<img width="533" height="221" alt="Screenshot 2025-09-22 at 3 58 34 PM" src="https://github.com/user-attachments/assets/a0622717-f081-420d-9203-8c2d19ff3f82" />


## Step 3: Configure Teams
- After creating your department you should already be on this page
- Since we are already in the Admin panel, go ahead and click the **Teams** tab

<img width="978" height="504" alt="Screenshot 2025-09-22 at 4 03 00 PM" src="https://github.com/user-attachments/assets/9e612ebb-5867-4b63-994d-3950af85aa03" />

- Click **Add new team**
- We are going to name this team **Online Banking**
- Click **Create Team**

<img width="491" height="290" alt="Screenshot 2025-09-22 at 4 04 12 PM" src="https://github.com/user-attachments/assets/072968e4-2efc-4fab-bf78-79b9d030f9a6" />

## Step 4: Allow end users to create tickets
<p>In this step we are going to configure the settings so that our end users can create tickets for themselves (even if they don't have a registered account)</p>

- Since we are already in the Admin panel, go ahead and click **Settings**
- Click **Users** (screenshot below)

<img width="538" height="149" alt="Screenshot 2025-09-22 at 4 08 14 PM" src="https://github.com/user-attachments/assets/a2f420f4-a9cd-4186-b38f-8a5180752488" />

- This next step is important
- Refer to the screenshot below and make sure that there is **no checkmark** next to "Require registration and login to create tickets"
- Click "Save Changes" only if there was previously a checkmark

<img width="703" height="524" alt="Screenshot 2025-09-22 at 4 09 44 PM" src="https://github.com/user-attachments/assets/c4166d5e-7e8f-4b51-9e03-3a5864492d1c" />

## Step 5: Configure Agents
<p>Next we are going to configure our agents, which are our workers. When we set this up you should see yourself as the only Agent in here so far. We are going to create more agents.</p>

- Click **Agents**
- Click **Add New Agent**

<img width="957" height="335" alt="Screenshot 2025-09-22 at 4 13 10 PM" src="https://github.com/user-attachments/assets/6f859641-159a-4dbc-8099-eae323de743b" />

- In this example we are going to create an agent named **Jane** and we are going to assign her the **SysAdmins** role
- Enter the credentials for your agent as well as their username
- Click **Access**

<img width="816" height="327" alt="Screenshot 2025-09-22 at 4 17 45 PM" src="https://github.com/user-attachments/assets/e8f75a75-e1b8-4350-9942-6fa3cd7633d1" />

- Select **SysAdmins**

<img width="199" height="204" alt="Screenshot 2025-09-22 at 4 19 41 PM" src="https://github.com/user-attachments/assets/add6c6ec-673c-487b-acff-656471a22eb7" />

- Select **Full Admin**
  
<img width="151" height="212" alt="Screenshot 2025-09-22 at 4 20 10 PM" src="https://github.com/user-attachments/assets/f0b99d00-7863-4045-8790-752b8c93691d" />

- Click the **Permissions** tab
- Note that everything is already checkmarked, so we don't need to do anything here

<img width="667" height="255" alt="Screenshot 2025-09-22 at 4 21 21 PM" src="https://github.com/user-attachments/assets/6818f8b1-14f0-4ffb-a6b1-68357d1c3335" />

- Click the **Teams** tab
- Click **Online Banking** for the team
- Click **Create**

<img width="667" height="286" alt="Screenshot 2025-09-22 at 4 22 01 PM" src="https://github.com/user-attachments/assets/e14b57fe-b414-4cb5-a171-92fd35c6668d" />


- Click the **Agents** tab, we are going to create one more Agent
- Click **Add New Agent**
- Add the appropriate credentials
- In my example our Agent will be John Doe

<img width="749" height="343" alt="Screenshot 2025-09-22 at 4 24 56 PM" src="https://github.com/user-attachments/assets/9db877b3-c201-4c66-8619-8a2232b43a0b" />

- Click the **Access** tab
- Select **Support** as John's department
- Select **All Access** for John's role
- Click **Create**
  
<img width="417" height="86" alt="Screenshot 2025-09-23 at 1 43 54 PM" src="https://github.com/user-attachments/assets/75316b7f-be19-47ec-833f-5f50028af654" />



## Step 6: Configure our Agents' passwords

- Click the **Agents** tab
- Click **Jane Doe** or whoever your first agent is
- Click **Set Password**
- Uncheck this (screenshot below)
- After unchecking, you should be prompted to type in Jane's password

<img width="303" height="43" alt="Screenshot 2025-09-22 at 4 30 55 PM" src="https://github.com/user-attachments/assets/4b7082cc-1662-4dcd-8881-49bec9394763" />

- Set Jane's password
- Click **Update**

<img width="645" height="284" alt="Screenshot 2025-09-22 at 4 32 04 PM" src="https://github.com/user-attachments/assets/95a7ec2e-e191-4737-86eb-de2b046b6775" />

- Click on the **Agents** tab
- We are going to do the same our second agent, **John Doe**
- Click **Set Password**
- Uncheck this (screenshot below)
- After unchecking, you should be prompted to type in John's password

<img width="303" height="43" alt="Screenshot 2025-09-22 at 4 30 55 PM" src="https://github.com/user-attachments/assets/4b7082cc-1662-4dcd-8881-49bec9394763" />

- Set John's password
- Click **Update**


## Step 7: Configure Users (customers)

- Click the **Agent Panel**
- Click the **Users** tab
- Click **Add User**

<img width="958" height="339" alt="Screenshot 2025-09-22 at 4 35 52 PM" src="https://github.com/user-attachments/assets/a206a555-3616-4f0b-bb8e-a85f1cdca57d" />

- Enter the name of your user, in my example the user's name is **Karen**
- Click **Add user**

<img width="640" height="391" alt="Screenshot 2025-09-22 at 4 37 17 PM" src="https://github.com/user-attachments/assets/cde8abcc-86fa-4efe-93b8-33bbbbd3db20" />


## Step 8: Configure SLA (Service Level Agreement)
<p>We are going to create 3 SLA plans each with a different severity.</p>
<p>Our Sev-A SLA plan will be on a 24/7 schedule to ensure that severe trouble tickets resolved as soon as possible without having to wait for the weekend.</p>
<p>Our Sev-B SLA plan will also be on a 24/7 schedule to ensure that important trouble tickets get resolved soon. These will be important but not as critical as the Sev-A SLA plan./p>
<p>Sev-C SLA will be on a normal working schedule, Monday - Friday at business hours for regular trouble tickets.</p>


- Click **Admin panel**
- Click the **Manage** tab
- Click the **SLA** tab
- Click **Add New SLA Plan**

<img width="954" height="226" alt="Screenshot 2025-09-22 at 4 42 23 PM" src="https://github.com/user-attachments/assets/e7fbfd7f-4014-49de-b2f1-d7bad1870ee3" />

- Name this SLA **Sev-A**
- Select **1 hour** for the grace period
- Select the **24/7** schedule
- Click **Add Plan**

<img width="640" height="256" alt="Screenshot 2025-09-22 at 4 49 01 PM" src="https://github.com/user-attachments/assets/a537df69-9ce6-4343-8ad1-4d58450a269c" />

- Click **Add New SLA Plan**
- Name this SLA **Sev-B**
- Select **4 hours** for the grace period
- Select the **24/7** schedule
- Click **Add Plan**

<img width="703" height="258" alt="Screenshot 2025-09-22 at 4 53 08 PM" src="https://github.com/user-attachments/assets/b5e21400-95d1-42be-bdf1-8b4cf32bd99e" />

- Click **Add New SLA Plan**
- Name this SLA **Sev-C**
- Select **8 hours** for the grace period
- Select **Monday - Friday 8am - 5pm with US Holidays**
- Click **Add Plan**

<img width="733" height="263" alt="Screenshot 2025-09-22 at 4 54 39 PM" src="https://github.com/user-attachments/assets/9570a305-ecd9-4b82-8f93-59fdb104872d" />



## Step 9: Configure Help Topics
- In this step we are going to configure a few help topics: 
  - Business Critical Outage
  - Personal Computer Issues
  - Equipment Request
  - Password Reset
  - Other

- Since we are already in the Admin Panel, click the **Manage** tab
- Click the **Help Topics** tab
- Click **Add New Help Topic**

<img width="995" height="453" alt="Screenshot 2025-09-22 at 4 58 14 PM" src="https://github.com/user-attachments/assets/9c8e90f5-8888-4cef-b46b-1f80222c3a9a" />

- Inside topic, type in **Business Critical Outage**
- Inside Parent topic, click **Report a Problem**
- Click **Add Topic**


<img width="717" height="482" alt="Screenshot 2025-09-22 at 5 01 20 PM" src="https://github.com/user-attachments/assets/56b193c8-295b-45e6-a903-f3e158b059b6" />


- Click the **Help Topics** tab
- Click **Add New Help Topic**
- Inside topic, type in **Personal Computer Issues**
- Inside Parent topic, click **Report a Problem**
- Click **Add Topic**

<img width="616" height="225" alt="Screenshot 2025-09-22 at 5 04 04 PM" src="https://github.com/user-attachments/assets/39869452-830e-4e2b-8027-40fbe83d9db5" />

- Click the **Help Topics** tab
- Click **Add New Help Topic**
- Inside topic, type in **Equipment Request**
- Inside Parent topic, click **General Inquiry**
- Click **Add Topic**
  
<img width="600" height="192" alt="Screenshot 2025-09-22 at 5 05 59 PM" src="https://github.com/user-attachments/assets/37cb2844-2241-4645-9991-8fbcc6ccce50" />

- Click the **Help Topics** tab
- Click **Add New Help Topic**
- Inside topic, type in **Password Reset**
- Inside Parent topic, click **General Inquiry**
- Click **Add Topic**

<img width="548" height="133" alt="Screenshot 2025-09-22 at 5 06 47 PM" src="https://github.com/user-attachments/assets/36a91ae6-6d38-43f5-bb35-bae7e0dad281" />

- Click the **Help Topics** tab
- Click **Add New Help Topic**
- Inside topic, type in **Other**
- Inside Parent topic, click **General Inquiry**
- Click **Add Topic**

<img width="564" height="129" alt="Screenshot 2025-09-22 at 5 07 34 PM" src="https://github.com/user-attachments/assets/9775c342-d991-49be-a1da-cc04d44d0da1" />



- That's it! We have set up our roles, departments, teams, agents, users, SLAs, and help topics.
- In the next lab we will be going over **Ticket Lifecycle** using osTicket and the configurations we did in this section.
- Link to Ticket Lifecycle section (to be added)


<br />
