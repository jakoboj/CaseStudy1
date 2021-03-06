# CaseStudy1

<h2>Hosting requirements</h2>
I created a windows virtual machine, and added IIS through the command:
<ul>
<li>Install-WindowsFeature -name Web-Server -IncludeManagementTools</li>
</ul>

![IIS](https://github.com/jakoboj/CaseStudy1/blob/main/Screenshots/IIS.PNG)

I also added inbound rules allowing access on port 80 and 443, for HTTP and HTTPS

![Inbound Rules](https://github.com/jakoboj/CaseStudy1/blob/main/Screenshots/Rules-Windows.PNG)

<br />
<br />

For the Linux virtual machine, I installed FTP with the commands:
<ul>
    <li>
        sudo apt update
    </li>
    <li>
        sudo apt install vsftpd
    </li>
</ul>


To check if FTP was installed correctly, I used the command:
<ul>
    <li>
        	sudo service vsftpd status
    </li>
</ul>

![FTP](https://github.com/jakoboj/CaseStudy1/blob/main/Screenshots/FTP.PNG)

I also added inbound rules allowing access on port 21 for FTP:

![Inbound Rules](https://github.com/jakoboj/CaseStudy1/blob/main/Screenshots/Rules-Linux.PNG)

<br />
<h2>Security requirements</h2>
For the security requirements I created a Firewall, with the following DNAT rules to restrict external access only to ports 80/21/443:

![DNAT Rules](https://github.com/jakoboj/CaseStudy1/blob/main/Screenshots/DNAT.PNG)

<br />

I also created a Bastion host to allow remote connections to the VMs:

![Bastion](https://github.com/jakoboj/CaseStudy1/blob/main/Screenshots/Bastion.PNG)

<br />
<h2>Backup</h2>
For backup I set up a Recovery Service vault, and added both the VMs:

![Backup](https://github.com/jakoboj/CaseStudy1/blob/main/Screenshots/Backup.PNG)

<br />
<h2>Storage</h2>
I created a storageaccount conatining a file share. This fileshare was mapped to the windows virtual machine through a powershell script.

<h2>Diagram</h2>

![Diagram](https://github.com/jakoboj/CaseStudy1/blob/main/Diagram/Diagram.PNG)

