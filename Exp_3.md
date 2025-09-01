# Expreiment 3 : Capture and Analyze Network Traffic using Wireshark

## Aim
The aim of this experiment is to capture and analyze network traffic passing through a network interface using the Wireshark software. The goal is to understand what data is being transmitted, identify the protocols in use, and examine the contents of individual packets.

## Description
This procedure involves setting up Wireshark to listen on a network interface card (NIC), capturing packets as they are sent and received, and then using Wireshark’s filtering and analysis features to inspect the captured data. We will look at different types of network protocols, such as TCP, UDP, and ICMP, and dissect the headers and payloads of these packets to understand how data is encapsulated and transmitted across a network.

## Tools & Equipment
A computer with a working network connection (Ethernet or Wi-Fi).

The Wireshark software package installed on the computer.

Administrative privileges on the computer to allow Wireshark to capture packets.

## Procedure
Launch Wireshark: Open Wireshark with administrative privileges.

Select Network Interface: On the main screen, you will see a list of available network interfaces (e.g., Ethernet, Wi-Fi). Select the interface you want to monitor, which is the one currently connected to the network.

Start Capture: Click the 'Start' button (often a shark fin icon) to begin capturing network traffic. Wireshark will immediately start displaying packets in real time as they traverse the selected interface.

Generate Traffic: To see interesting data, you need to generate some network activity. You can do this by browsing a website, opening an application that connects to the internet, or pinging a server.

Stop Capture: Once you have captured enough data (usually after a few minutes), click the 'Stop' button (a red square) to halt the capture process.

Analyze Packets:

Packet List Pane (Top): This pane shows a summary of each captured packet. You can click on a packet to select it.

Packet Details Pane (Middle): This pane provides a detailed breakdown of the selected packet's layers (e.g., Ethernet, IP, TCP/UDP). Expand these layers to see the header information and fields.

Packet Bytes Pane (Bottom): This pane shows the raw hexadecimal data of the packet, with the corresponding ASCII characters.

Apply Filters: Use the display filter bar at the top to narrow down the captured traffic. For example, typing http will show only HTTP traffic, and ip.addr == 192.168.1.1 will show traffic to or from a specific IP address.

Save the Capture: Save the captured packets in a file (with a .pcap or .pcapng extension) for future analysis.

## Result Experiment
The result of this experiment is a captured network trace file that provides a comprehensive view of the network traffic. By analyzing this data, you will be able to identify the protocols in use, the source and destination of the traffic, and the contents of the data being transmitted. This is a crucial skill for diagnosing network issues, monitoring for security threats, and understanding how different applications communicate over a network.