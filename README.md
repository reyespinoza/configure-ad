<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy Active Directory within Azure Part I](https://www.youtube.com/watch?v=1bVKsDV1qOY)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/nApUd9H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to your Azure account: https://portal.azure.com so we can begin creating our resources.  Select the Virtual Machines icon or type 'Virtual Machines' in the search box.
</p>
<br />

<p>
<img src="https://i.imgur.com/8W2fesq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click on the drop down arrow next to 'Create' and select Azure virtual machine
</p>
<br />

<p>
<img src="https://i.imgur.com/fKsd4SJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the 'Basics' tab, you will select 'Create New' under 'Resource Group' and name your Resource group 'AD-Lab'.  Give your VM the name 'DC1' (domain controller).  Select whichever region you prefer.
</p>
<br />

<p>
<img src="https://i.imgur.com/oxdNFJH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the 'Image' section, select a Windows Server image.
</p>
<br />

<p>
<img src="https://i.imgur.com/9ql4koc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For 'Size', select a size with 2 vcpus.  If you are using the free trial, you may only be able to use a total of 4 vcpus.  Keep this in mind as we will be using two VMs.
</p>
<br />

<p>
<img src="https://i.imgur.com/dg0nwmm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a username and password for your administrator.  Remember to keep simple for training purposes.  Then, select review and create.  Wait for the validation process and select 'Create'
</p>
<br />

<p>
<img src="https://i.imgur.com/IyVD5U3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you select 'Create', wait for your resources to start populating.  After you see your resources start to appear, select 'Home' and we will begin creating our second VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/txQ4ace.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Home tab, select virtual machines and create a virtual machine.  Select the same resource group as the previous VM (AD-Lab).  Give your new VM a name and select the same region as your previous VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/THABInW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For image, this time we select Windows 10 Pro.
</p>
<br />

<p>
<img src="https://i.imgur.com/ckfIUvk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Assign a username and password for your administrator.
</p>
<br />

<p>
<img src="https://i.imgur.com/2IsaySm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select 'Next: Disks>'
</p>
<br />

<p>
<img src="https://i.imgur.com/JW7QbFN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select 'Next: Networking>'
</p>
<br />

<p>
<img src="https://i.imgur.com/L1iRfwo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the 'Networking' tab, you want to make sure that the Virtual network that was created from our initial Resource group is selected.  In this case, Ad-Lab-vnet. Go back to the 'Home' tab.
</p>
<br />

<p>
<img src="https://i.imgur.com/7lCPcnb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You will receive a notification that your VMs have been created.  If you didn't see your notitication, click on the notifications icon and confirm that your VMs have been created.  Select the Virtual machines resource tab to view your VMs.
</p>
<br />

<p>
<img src="https://i.imgur.com/dUUMEzi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click on your domain controller VM.  In this case, DC-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/Z9hIbyb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you select DC-1, you will click on the Networking blade under the Settings tab.
</p>
<br />

<p>
<img src="https://i.imgur.com/TfFPyLT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, select the Network Interface (NIC) for the VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/A8SbKls.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You will then select the IP configurations blade under the Settings tab.
</p>
<br />

<p>
<img src="https://i.imgur.com/QkR7SlL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once in the configuations blade, we will change the IP assignment from 'Dynami' to 'Static'.  We don't want our domain controller's IP address to change.
</p>
<br />

<p>
<img src="https://i.imgur.com/5g7ewKN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select 'Save'
</p>
<br />

<p>
<img src="https://i.imgur.com/fEX8lvr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select 'Home'
</p>
<br />

<p>
<img src="https://i.imgur.com/xWHca8e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select Virtual machines or use the search box and type in virtual machines.
</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
<img src=" " height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />
