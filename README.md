# pfSense Firewall Lab (Cybersecurity Home Lab)

This project is to demonstrate how I built a home lab using virtual machines to simulate an attack and how to stop it using a firewall.

## 🎯 Objectives
The goal is to simulate a Denial of Service (DoS) attack and then block it using firewall rules.
Build a virtual network with separate internal and external zones
Simulate an attack from an external machine
Monitor live network traffic
Apply firewall rules to stop malicious activity

## 🧰 Tools & Technologies
VirtualBox (Virtualization)

pfSense (Firewall)

Kali Linux (Attacker)

Ubuntu Desktop (Victim)

Wireshark (Traffic Analysis)

## 🖼️ Network Topology
        [ Kali Linux (Attacker) ]
                  |
            (External Network)
                  |
             [ pfSense ]
          (Firewall / Router)
                  |
            (Internal Network)
                  |
        [ Ubuntu (Victim) ]
        
## ⚙️ Lab Setup
**1. Create Virtual Machines**

Set up three virtual machines in VirtualBox:

-pfSense

-Kali Linux
Network: Bridged

-Ubuntu Desktop
Network: Internal Network

**2. Configure pfSense**

Assign WAN and LAN interfaces

Enable DHCP on LAN

**3. Allow traffic temporarily for testing**

**4. Verify Connectivity**

Ensure Ubuntu receives an IP from pfSense

Test connectivity from Kali to Ubuntu using ping

## 💥 Simulating the Attack

From the Kali machine, launch a traffic flood toward the Ubuntu system:

ICMP flood (ping-based)

SYN flood (web traffic simulation)

Use Wireshark on Ubuntu to observe:

Large spikes in incoming packets

Signs of network congestion

## 🛑 Blocking the Attack

In pfSense:

Navigate to firewall rules

Create a rule to block traffic from the attacker (Kali)

Apply changes

## ✅ Result:
Traffic immediately stops

Wireshark no longer shows the attack

Firewall logs confirm blocked traffic

## 📊 What I Learned

I was able to simulate a DoS attack

Observed attack behavior in real time

Prevented the attack using firewall rules


## 👤 Author

Raudy Martinez

GitHub: raudy82
