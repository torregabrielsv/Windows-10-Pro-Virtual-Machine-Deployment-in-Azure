# Windows-10-Pro-Virtual-Machine-Deployment-in-Azure
This project provides a detailed walkthrough for creating and configuring a Windows 10 Pro virtual machine (VM) in Microsoft Azure. The aim is to guide users through the process of setting up a VM with specific configurations, including selecting appropriate sizes, creating a secure environment, and organizing resources effectively within Azure.

![Screenshot 2024-07-29 at 7 45 30 AM](https://github.com/user-attachments/assets/8bd493d0-2e20-450b-8a83-05bada1f2dbe)

Languages Used:
•	PowerShell: To automate the deployment process and manage Azure resources.
•	Azure CLI: For command-line operations to configure and manage the VM and related resources.
Environments Used:
•	Azure: The primary environment for creating and managing the virtual machine and associated resources.
Technology/Applications/Services Used:
•	Azure Virtual Machines: To host the Windows 10 Pro VM.
•	Azure Resource Groups: For organizing and managing related resources.
•	Azure Virtual Network: For setting up a virtual network to connect the VM.
Configuration Details:
1.	Virtual Machine Name: FINAL-VM
2.	Region: East US 2
3.	Resource Group Name: RG-FINAL-LAB
4.	Virtual Network Name: FINAL-VM-vnet
5.	VM Size: Select an appropriate size that balances cost and performance (e.g., B-series for cost-effectiveness).
6.	Password: Create a strong password to ensure security.
The project will include detailed instructions on each of these steps, ensuring that users can deploy and configure their Windows 10 Pro VM effectively.

### Instructions for Creating a Windows 10 Pro Virtual Machine in Azure

#### **1. Sign In to Azure Portal**

1. Go to the [Azure Portal](https://portal.azure.com).
2. Sign in with your Azure account credentials.

<img width="1440" alt="1 2  Sign in with your Azure account credentials" src="https://github.com/user-attachments/assets/f9b4e5ab-37aa-43bd-abe0-47b00c9c35c0">

#### **2. Create a Resource Group**

1. **Navigate to Resource Groups:**
   - In the Azure Portal, search for **"Resource groups"** in the search bar at the top of the page and select it.

2. **Create a New Resource Group:**
   - Click on **"Create"**.
   - **Resource Group Name:** Enter `RG-FINAL-LAB`.
   - **Region:** Select **East US 2**.
   - Click **"Review + Create"**, then **"Create"**.

<img width="951" alt="2  **Create a New Virtual Network:**" src="https://github.com/user-attachments/assets/df8b54db-4c81-45a9-a812-05f716ec77e2">

#### **3. Create a Virtual Network**

1. **Navigate to Virtual Networks:**
   - In the Azure Portal, search for **"Virtual networks"** in the search bar and select it.

   - Click on **"Create"**.
   - **Subscription:** Ensure your subscription is selected.
   - **Resource Group:** Select `RG-Cyber-Lab`.
   - **Name:** Enter `FINAL-VM-vnet`.
   - **Region:** Select **East US 2**.
   - **IP Addresses:**
     - **Address space:** Enter a valid IP range (e.g., `10.0.0.0/16`).
     - **Subnet:** Enter a subnet name (e.g., `default`) and IP range (e.g., `10.0.0.0/24`).
   - Click **"Review + Create"**, then **"Create"**.

<img width="951" alt="3  Create a Virtual Network" src="https://github.com/user-attachments/assets/efffdf8b-67c9-4c59-b8d6-3f11a7523409">

#### **4. Create a Windows 10 Pro Virtual Machine**

1. **Navigate to Virtual Machines:**
   - In the Azure Portal, search for **"Virtual machines"** in the search bar and select it.

2. **Create a New Virtual Machine:**
   - Click on **"Create"**, then **"Azure virtual machine"**.

3. **Basics Tab:**
   - **Subscription:** Ensure your subscription is selected.
   - **Resource Group:** Select `RG-FINAL-LAB`.
   - **Virtual Machine Name:** Enter `FINAL-VM`.
   - **Region:** Select **East US 2**.
   - **Image:** Select **Windows 10 Pro** from the drop-down list.
   - **Size:** Click **"Change size"** and choose an appropriate VM size (e.g., `B2s` for cost-effectiveness). Click **"Select"**.
   - **Authentication Type:** Select **Password**.
   - **Username:** Enter a username (e.g., `labuser`).
   - **Password:** Enter a strong password and confirm it (e.g., a combination of uppercase, lowercase, numbers, and special characters). (e.g., Cyberlab123!)
   - **Inbound port rules:** Select **Allow selected ports** and choose **RDP (3389)** to enable remote desktop access.

4. **Disks Tab:**
   - **OS Disk Type:** Select the appropriate type (e.g., **Standard SSD** or **Premium SSD**).
   - Leave other settings as default or adjust based on your needs.

5. **Networking Tab:**
   - **Virtual Network:** Select `FINAL-VM-vnet`.
   - **Subnet:** Choose the default subnet or create a new one if needed.
   - **Public IP:** Select **Create new** if you need a public IP address for RDP access.
   - **NIC network security group:** Choose **Basic** and configure any necessary rules (e.g., allowing RDP access).

6. **Management Tab:**
   - Configure monitoring and management options based on your needs. Default settings are typically sufficient for most use cases.

7. **Review + Create:**
   - Review all your configurations.
   - Click **"Create"** to deploy the VM.

<img width="1552" alt="4  Create a Windows 10 Pro Virtual Machine" src="https://github.com/user-attachments/assets/a3fff9ad-f4d8-47c0-9a56-7f25519bdf52">

#### **5. Connect to Your Virtual Machine**

1. **Navigate to Virtual Machines:**
   - In the Azure Portal, go to **"Virtual machines"**.

2. **Select Your VM:**
   - Click on `FINAL-VM` to open the VM’s details page.

3. **Connect to the VM: (On Mac)**
   1. Open **Microsoft Remote Desktop** on your Mac.
   - Click on the **"+"** button to add a new connection and select **"Add PC"**.
   - In the **"PC name"** field, enter the IP address or hostname of the VM.
   - Enter the username and password you created during the VM setup in the **"User Account"** section.
   - Click **"Add"** to save the connection.
   2. Select the newly added VM from the list and click **"Start"** to connect.
   - You may need to click **"Continue"** or **"OK"** to proceed with the connection.
You have now successfully created and configured a Windows 10 Pro virtual machine in Azure.

<img width="711" alt="5  Connect to Your Virtual Machine" src="https://github.com/user-attachments/assets/f23049aa-5cc8-42a2-91b9-76ee22dc5a6a">

<img width="1440" alt="5 last" src="https://github.com/user-attachments/assets/aa784fad-14a0-4579-ad87-f771c3fe37ae">












