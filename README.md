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

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Configuration Steps</h2>

## Step 1: Configure Roles

<p>We are going to be using this link to log into our <a href="http://localhost/osTicket/scp/login.php">admin page</a>.</p>
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
<p>In this step we are going to add a few roles, including: **SysAdmins**</p>

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



















<br />
