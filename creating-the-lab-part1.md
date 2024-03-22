<h2>Required Preliminary Steps To Set Up The Lab:</h2>
<li>Get Oracle VirtualBox, Windows Server and Client isos</li>
<li>Install 2 Virtual Machines (Server and at least one Client)</li>

<h2>First Steps</h2>

<li>In VirtualBox, enable a second Ethernet Adapter for an internal network</li>
<img src="https://i.imgur.com/grLHcqZ.png">

<li>Install VirtualBox Guest Additions so that the whole virtual experience is more smooth</li>

<li>Really good idea: After the server is installed, create a snapshot to revert to if you break something (and you will)</li>
<img src="https://i.imgur.com/RRjjcdv.png">

<li>Greeted by the Server Manager. Change some names, so that you wont get confused. (some restarts required)</li>
<img src="https://i.imgur.com/OyRKTBp.png">

<img src="https://i.imgur.com/sp6LKjt.png">
Less confusing this way...

<h2>Setting up a static IP address for the server</h2>

<li>In order for the internal network to function, you need to manually set the IP of the server like this:</li>
<img src="https://i.imgur.com/k8XLhxD.png">
We are using the subnet 172.16.0.xxx and our server will function as the DNS server as well, which is why the loopback address is used 

<h2>Assigning the role of Domain Controller to the server</h2>
<li>In the main window, select "add roles and features"</li>
<li>choose active directory domain services and proceed with the installation</li>
<img src="https://i.imgur.com/Nr1UmBF.png">

<li>after the installation is successful, you'll need to actually promote the server to domain controller:</li>
<img src="https://i.imgur.com/Q61PVdi.png">

<li>This is the part where you name your domain. The wizard will also configure the DNS server in the installation process</li>
<img src="https://i.imgur.com/Mi5tVXr.png">

<li> The machine automatically restarts here and when it's done with everything, your Domain is almost ready</li>

<h2> Continued in part 2 . . . </h2>
