<h2>Installing RAS / NAT</h2>

<li>Why? Because our client machine only use our internal network and wont have access to the internet</li>
  (the server has one network setup in virtualbox that uses the hosts NAT, so it gets access to the internet through your actual PC)
<li>so we are setting up a virtual NAT for our virtual internal network. our server will provide NAT for our clients</li>

<li>First thing is to add a new role. The one we are looking for is Remote Access</li>
<img src="https://i.imgur.com/fLXnGlt.png">
<li>click your way through the wizard and select <b>Routing</b> in the Role Services portion. RAS will be selected automatically</li>
<img src="https://imgur.com/0T2muUA.png">

<li>after the wizard finishes his job, we need to configure the NAT service. go to Tools and select Routing and Remote Access</li>
<img src="https://i.imgur.com/s7Ww3bN.png">

<li>go to the configuration window of your server</li>
<img src="https://i.imgur.com/HJyVTFy.png">

<li>and select the NAT service to configure</li>
<img src="https://i.imgur.com/hl5XWAS.png">

<li>now select the virtual ethernet adapter that routes to your host machine's internet access. this way we can reroute it again towards our client machines on the virtual internal network</li>
<img src="https://i.imgur.com/i8bY4af.png">


<h2>Setting up DHCP - Dynamic Host Configuration Protocol</h2>
<li>we are almost done. The next piece of the puzzle is the DHCP server. This will assign private IP addresses to our client machines so that they can function in the internal network.</li>
<li>same old game - add a new role; this time it's the DHCP server</li>
<img src="https://i.imgur.com/qxu0Jju.png">

<li>after the installation is complete, you can search for DHCP in your tools and right click on IPv4 to create a <b>new scope</b></li>
<li>for the name, it helps to use the actual scope range as the name so in this instance:</li>
<img src="https://i.imgur.com/BhRCQLl.png">
<li>define the start and end IP addresses like so and give it a mask of 24</li>
<img scr="https://i.imgur.com/3B999rC.png">
<li>the wizard will ask you if you want to configure DHCP options - you do. this is where we can configure which server the clients will use for DNS and the gateway. In this case we want to to be our one and only server we've been configuring</li>
<li>so when asked, put in the IP address that we manually set for our server like so. dont forget to click add</li>
<img src="https://i.imgur.com/wmjR1RF.png">

<li>when we added active directory to our server, it already installed DNS and because of that, it already is found in the next window here. you dont need to change anything</li>
<img src="https://i.imgur.com/XGWQxJW.png">

<li>now, after going through the wizard, the final touch is to right click your domain controller and click 'authorize'.</li>
<img src="https://i.imgur.com/MJyIv4C.png">

<li>and now we've pretty much done it. The server is ready to be populated with clients. When one joins the domain, it will get a private IP address from the DHCP server, find the router to use its NAT table to connect to the internet and through the DNS server, be visible by its name instead of only its IP. sweet!</li>
