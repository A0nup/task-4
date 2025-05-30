# task-4
Objective:
Configure and test basic firewall rules to allow or block network traffic.

Tools Used:
OS: Kali Linux
Firewall: UFW (Uncomplicated Firewall)
Testing Tool: Telnet, netcat-traditional

Steps Performed:
1.Enabled UFW Firewall
sudo ufw enable

2.Listed Current Firewall Rules
sudo ufw status numbered

3.Blocked Inbound Traffic on Port 23 (Telnet)
sudo ufw deny 23

4,Installed & Ran Netcat on Port 23
sudo apt install netcat-traditional
sudo nc -l -p 23

5.Tested Block Using Telnet
In another terminal:
telnet localhost 23
Connection was refused (blocked by firewall)

6.Allowed SSH (Port 22)
sudo ufw allow 22

7.Removed the Test Rule (Optional Cleanup)
sudo ufw delete deny 23

🔍 Firewall Filtering Summary:
The firewall uses defined rules to allow or deny traffic based on ports, IPs, and protocols. In this task, UFW blocked Telnet on port 23, demonstrating how a firewall protects systems by filtering unwanted traffic.

