<h2>FSMO Roles</h2>

<li>the Flexible Single Master Operations or FSMO are special roles that are assigned to single Domain Controllers throughout the forest</li>
<li>there are read only copies of each of these objects on all servers, but only one writable one can exist at one time.</li>
<li>the FSMO are:</li>
<li>DOMAIN NAMING MASTER</li>
<li>SCHEMA MASTER</li>
<li>RID MASTER</li>
<li>INFRASTRUCTURE MASTER</li>
<li>PDC EMULATOR MASTER</li>

<img src="https://i.imgur.com/K5acr5w.png"> 
by right clicking your domain you can view the RID, PDC and Infrastructure FSMO
<img src="https://i.imgur.com/WbkNsWF.png">
<p>In this case all three are assigned to the main DC server</p>


<li>the domain naming master can be viewed by going to Active Directory Domains and Trusts and right clicking the first object on the left </li>
<img src="https://i.imgur.com/tn6ZIAP.png">

<p>
  <li>the schema master is hidden by default so you'll have to go through some steps to make it visible</li>
  <li>first we need to register a .dll file like this</li>
  <img src="https://i.imgur.com/CqUjNLU.png">
  <li>then go to the MMC and add the Active Directory Schema as a snap-in </li>
  <img src="https://i.imgur.com/sS10EI9.png">
  <li>and there it is. right click the schema snap-in and you can check out the operations master</li>
  <img src="https://i.imgur.com/XH2TWL3.png">
</p>

