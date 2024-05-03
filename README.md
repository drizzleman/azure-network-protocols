# azure-network-protocols# Network-Security-Groups-NSGs-and-Inspecting-Traffic-Between-Azure-Virtual-Machines<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>


In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1- Create resource group in Microsoft Azure
- Step 2- Create two virtual Machines in Azure
- Step 3- Download Wireshark once VMs are created 
- Step 4- Use wireshark to filter network traffic 

<h2>Actions and Observations</h2>

<p>
<img width="941" alt="image" src="https://github.com/drizzleman/Network-Security-Groups-NSGs-and-Inspecting-Traffic-Between-Azure-Virtual-Machines/assets/166667455/011e8179-0a31-4c7c-895f-ab0b5ebb3ccb">

</p>
<p>
Go to google.com and search wireshark. Download latest verison of wireshark and once completed open app and click Ethernet to start filtering network traffic.
</p>
<br />

<p>
<img width="943" alt="image" src="https://github.com/drizzleman/Network-Security-Groups-NSGs-and-Inspecting-Traffic-Between-Azure-Virtual-Machines/assets/166667455/0a21349a-25e9-41d0-be93-97a237567db0">

</p>
<p> Create a perpeatual ping in powershell to see the traffic flow between VM1 and VM2 by using VM2 private IP address.The traffic will filter inside of wireshark with the ICMP command.
</p>
<br />

<p>
<img width="941" alt="image" src="https://github.com/drizzleman/Network-Security-Groups-NSGs-and-Inspecting-Traffic-Between-Azure-Virtual-Machines/assets/166667455/abb5d7d2-cc65-4863-b276-84e35413011f">

</p>
<p> Create a firewall in Microsoft Azure by going to Network security groups and select VM2. Select add and click ICMP under protocol and select deny under action. set the priority as you see fit and give a name then add the rule.
</p>
<br />
<p>
<img width="923" alt="image" src="https://github.com/drizzleman/Network-Security-Groups-NSGs-and-Inspecting-Traffic-Between-Azure-Virtual-Machines/assets/166667455/9dcda147-38a3-4741-8ce7-e76564a103b9">


</p>
<p> As you can onces the firewall is established the ping and wireshark traffic will start to timeout.
</p>
<br />
<p>
<p>
<img width="950" alt="image" src="https://github.com/drizzleman/Network-Security-Groups-NSGs-and-Inspecting-Traffic-Between-Azure-Virtual-Machines/assets/166667455/10ec82df-0fef-414f-9d62-162926a5d820">



</p>
<p> Next you can use SSH from VM1 to remote into VM2 using powershell and filter the traffic using wireshark.
</p>
<br />

</p>

</p>
<br />
