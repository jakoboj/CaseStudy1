# CaseStudy1

<h2>Hosting requirements</h2>
I created a windows virtual machine, and added IIS through the command:
<ul>
<li>Install-WindowsFeature -name Web-Server -IncludeManagementTools</li>
</ul>
I also added inbound rules allowing access on port 80 and 443, respectively for HTTP and HTTPS

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

