<p align="center">
<img src="https://imgur.com/in6BVUo.png" height="50%" width="50%" alt="Traffic Examination"/>
</p>

<h1 align="center">This Tutorial is a continuation from: <br> <a href="https://github.com/OKALLEY/configure-ad">Configuring Active Directory within Azure VMs</a>
</h1>
<br>
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
<img src="https://imgur.com/19phcqk.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
<li>Click on "_ADMINS" and right click inside the folder then under "New" select "User"</li>
<img src="https://imgur.com/prVV4W4.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<li>Name your administrator and create a User logon name <br> 
  appropriate to your company policy (e.g. jane doe; jane_admin or a-jane)</li>
<img src="https://imgur.com/5219Vay.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>
<li> Set the password. Normally the user would be required to change it, <br> but for this demonstration the password is set to never expire</li>
<img src="https://imgur.com/mDhVUC4.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
  
<li>Click on "Finish" once you have this completed</li>  
<img src="https://imgur.com/0eGHYrO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
  
<li>To make this name a administrator it needs to be assigned to the domain admins group. <br>
  Right click on it and go to "Properties" </li>   
<img src="https://imgur.com/3yrYOqc.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
  
<li>Click on "Member Of" and then "Add..."</li>  
<li>Find the section labeled "Enter the object names to select(examples):"</li> 
<li>In this section type "domain" and click "Check Names"</li>  
<img src="https://imgur.com/SVaLlb8.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<li>In the next window choose "Domain Admins" click "OK" and then "OK", "Apply" and then "OK"</li>
<img src="https://imgur.com/Hm8PDrd.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
  
<li>Next Log out / close the connection to DC-1 and log back in as "mydomain.com\jane_admin"</li>
<li>Go back to portal.azure.com and copy the DC-1 Public IP address,<br>
  access Remote Desktop Connection and paste it and click "Connect"</li>
<li>Click on "More choices" choose "Use a different account"<br> 
  and logon as "mydomain.com\jane_admin" </li>
<img src="https://imgur.com/JodJx1B.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<li>Click "OK" and then "Yes"</li> 
<img src="https://imgur.com/DwJSbOS.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

<h2>Join Client-1 to the Domain</h2>  
 <li>From the Azure portal set Client-1's DNS settings to the domain controller's (DC-1) Private IP address</li> 
 <li>Go to Virtual machines, click on DC-1 and click Networking</li>
 <li>Locate and copy the NIC Private IP</li>
 <img src="https://imgur.com/wp44R6G.png" height="90%" width="90%" alt="Disk Sanitization Steps"/>
 
 <p>

  <li>Go back to Virtual machines and click on Client-1 and choose Networking</li>
<li>Find "Network Interface:" and click on the client</li>
<img src="https://imgur.com/1lUWlxX.png" height="90%" width="90%" alt="Disk Sanitization Steps"/>
<li>Click DNS servers and under "DNS servers" click Custom and paste in the domain controller's Private IP address and then click "Save"</li>
<img src="https://imgur.com/IR5Q6xe.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
  

 
<li>To change the domain click Start and </li>    
