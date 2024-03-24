<h2>Lets get organized</h2>

<li>Now that we have our domain set up, we want to build a structure that closely follows best practices of real world domains in offices and companies</li>
<li>Commonly inside your domain, you want to create an OU (Organizational Unit) with the same name as your domain and place 2 OUs inside it - one for Users and one for Computers</li>
<img src="https://i.imgur.com/iLCGq30.png">
<li>Why do it like that? Because we want to add group policies to those OUs later and the default "Computers" and "Users" are containers that cant have GPs attached to them.</li>
