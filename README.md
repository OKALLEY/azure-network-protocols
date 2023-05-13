<p align="center">
<img src="https://imgur.com/in6BVUo.png" height="50%" width="50%" alt="Traffic Examination"/>
</p>

<h1 align="center">This Tutorial is a continuation from: <br> <a href="https://github.com/OKALLEY/configure-ad">Configuring Active Directory within Azure VMs</a>
</h1>
<p align="center"> ~In this tutorial, we will create Oraganizational Units (OU), Administrators and Employees.~
</p>
<br />
<h2>Configuration Steps</h2>

<ul>
  <li type =circle>Create an Administrator and a User Account in Active Directory<br>
  <li type =circle>Join Client-1 to Domain<br>
  <li type =circle>Setup Remote Desktop for Non-admin Users<br>
  <li type =circle>Concluding Assignment<br>
</ul>

<h2>Create an Administrator and a "Normal User" Account in Active Directory</h2>

<li>Login to the Domain Controller (DC-1) as user: mydomain.com\Lab USer</li>
<li>Click on Tools and click "Active Directory Users and Computers" </li>
<p>
<img src="https://imgur.com/3zrM8Ua.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<li>To create your first Oraganizational Unit right click on your domain <br>(e.g. mydomain.com) and under "New" click "Organizational Unit"</li>
<img src="https://imgur.com/HbM3U4h.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<li>Enter the name "_EMPLOYEES" and click "OK"</li>
<img src="https://imgur.com/5IwEAJG.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<li>Repeat these steps and make AN Oraganizational Unit named "_ADMINS"</li>
<img src="https://imgur.com/0ZNjzBY.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<lki>Right click your domain (e.g. mydomain.com) and click "Refresh"</li>
<img src="https://imgur.com/19phcqk.png" height="20%" width="20%" alt="Disk Sanitization Steps"/>
