<h2>Let's populate our domain</h2>

<h3>Adding another server</h3>
<li>Our first server is all alone in its domain, acting as the DC, DNS Server, DHCP Server and so on...</li>
<li>Let's share the load and set up another server that's going to join the domain</li>
<li>firstly, we are creating another virtual machine running windows server 22</li>
<li>after it's installed and ready to go, we're gonna change its name to something like "SVR-1"</li>
<li>then, in order for it to be able to join the domain we need to point it to the DNS Server. In our case it's our DC server.</li>
<li>so head over to that machine and get its IP address with your preferred method. </li>

<img src="https://i.imgur.com/RP7LVVF.png">
<li>here I opened up the basic command prompt and typed in "ipconfig"</li>
<li>this reveals your server's ipv4 address, which the new server needs to be pointed to for DNS services</li>

<img src="https://i.imgur.com/1m7e679.png">
<li>and this is where we are inputting that ip.</li>

<li>the next step is actually joining the domain.</li>
<li>so in your local server's settings, click the WORKGROUP text, go to Change and put in the name of your domain.</li>

<img src="https://i.imgur.com/1m7e679.png">
<li>next it will ask you to log in with credentials of that domain.</li>

<img src="https://i.imgur.com/lfxGxMN.png">
<li>and there you go. a new server joined the domain!</li>
