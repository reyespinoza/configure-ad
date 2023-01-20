<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com/channel/UCnqHxB12njtUur_VrjL5EtQ)

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
In the 'Basics' tab, you will select 'Create New' under 'Resource Group'.  Give your VM the name 'DC1' (domain controller).  Select whichever region you prefer.
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
Create a username and password for your administrator.  Remember to keep simple for training purposes.
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
