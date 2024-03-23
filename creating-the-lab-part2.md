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
