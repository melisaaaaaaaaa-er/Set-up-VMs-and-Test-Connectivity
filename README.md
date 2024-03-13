# Set-up VMs and Test Connectivity

<h2>Setting up Resources in Azure</h2>

<h3>DC-1 and Client-1</h3>

![1](https://github.com/melisa-er/Set-up-VMs-and-Test-Connectivity/assets/157723219/8f69bfb3-de7c-4ef0-b4c3-24e0e9a5fb91)

![2](https://github.com/melisa-er/Set-up-VMs-and-Test-Connectivity/assets/157723219/0fac2460-f5a2-4342-8d24-d0fbaecbc99b)

When setting up DC-1, make note of the resource group and vnet that the machine is assigned to. Client-1  needs to be using the same resource group and vnet.

<h3>DC-1 static IP</h3>

![3](https://github.com/melisa-er/Set-up-VMs-and-Test-Connectivity/assets/157723219/b9c9b0b6-622a-4633-acd8-2ee591bfaab8)

![4](https://github.com/melisa-er/Set-up-VMs-and-Test-Connectivity/assets/157723219/2fe01457-8ed0-4d7e-95cc-c30cde111e64)

![5](https://github.com/melisa-er/Set-up-VMs-and-Test-Connectivity/assets/157723219/8162b3eb-7424-4791-8647-3760cc321baa)

![6](https://github.com/melisa-er/Set-up-VMs-and-Test-Connectivity/assets/157723219/c39e11ac-7583-4283-8eba-501db4599bcf)

Change the private IP settings for DC-1 from dynamic to static.

Network servers should not use dynamic IP addresses as that could result in a change of IP address leading to clients on the network being unable to locate the server (like a business regularly changing their phone number – no one would be able to contact them!).

#
<h2>Testing Connectivity between DC-1 and Client-1</h2>

![7](https://github.com/melisa-er/Set-up-VMs-and-Test-Connectivity/assets/157723219/107bb3c3-c249-4207-b5d4-9ced06d780e0)

Login to Client-1 through Remote Desktop and try to ping DC-1 with a perpetual ping. The ping will initially be rejected by DC-1.

![8](https://github.com/melisa-er/Set-up-VMs-and-Test-Connectivity/assets/157723219/08ed01b7-4845-4748-a2ac-efadb1fb1f1e)

Login to DC-1 through Remote Desktop and configure Windows Firewall to permit ping/ICMP packets.

#
![9](https://github.com/melisa-er/Set-up-VMs-and-Test-Connectivity/assets/157723219/d3ae23f1-7b99-4093-a139-c3f7ddd909da)

Go back to Client-1. The ping request will go through after changing DC-1’s firewall settings.
