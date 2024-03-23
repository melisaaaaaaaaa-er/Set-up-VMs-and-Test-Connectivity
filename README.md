# Set-up VMs and Test Connectivity

<h2>Setting up Resources in Azure</h2>

<h3>DC-1 and Client-1</h3>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/1.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/2.png"/>

When setting up DC-1, make note of the resource group and vnet that the machine is assigned to. Client-1  needs to be using the same resource group and vnet.

<h3>DC-1 static IP</h3>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/3.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/4.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/5.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/6.png"/>

Change the private IP settings for DC-1 from dynamic to static.

Network servers should not use dynamic IP addresses as that could result in a change of IP address leading to clients on the network being unable to locate the server (like a business regularly changing their phone number – no one would be able to contact them!).

#
<h2>Testing Connectivity between DC-1 and Client-1</h2>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/7.png"/>

Login to Client-1 through Remote Desktop and try to ping DC-1 with a perpetual ping. The ping will initially be rejected by DC-1.

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/8.png"/>

Login to DC-1 through Remote Desktop and configure Windows Firewall to permit ping/ICMP packets.

#
<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/9.png"/>

Go back to Client-1. The ping request will go through after changing DC-1’s firewall settings.
