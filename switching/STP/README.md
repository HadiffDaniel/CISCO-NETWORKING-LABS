### **Spanning Tree Protocol (STP) Lab**





##### **Overview**



This lab focuses on configurating and verifying **Spanning Tree Protocol (STP)** on Cisco Switches.



The purpose of this lab is to understand how STP prevents Layer 2 switching loops while maintaining redundant pathes between switches.



The lab uses **Rapid PVST+** and includes VLAN segmentation, trunk configuration, native VLAN configuration, STP root bridge selection, and basic Layer 2 security features.





##### **Objectives**



* Understand the purpose of Spanning Tree Protocol (STP)
* Configure VLANs on Cisco Switches
* Configure 802.1Q trunk links
* configure dedicated native VLAN
* configure Rapid PVST+
* Configure the Root Bridge for a VLAN
* Identify Root Ports, Designated Ports, and Alternate Ports
* Verify STP operation using Cisco IOS commands
* Configure portfast and BPDU Guard on end-device ports
* secure unused switch ports





##### **Technologies \& Concepts**



* Cisco IOS
* VLAN
* IEEE 802.1Q Trunking
* Spanning Tree Protocol
* Rapid PVST+
* Root Bridge
* Root Port
* Designated Port
* Alternate Port
* Native VLAN
* PortFast
* BPDU Guard
* Layer 2 Security





##### **VLAN Configuration**



|VLAN|Name|Purpose|
|-|-|-|
|10|VLAN-10|Lab VLAN|
|20|VLAN-20|Lab VLAN|
|999|UNUSED-NATIVE|Native VLAN|



VLAN 999 is used as the native VLAN instead of using a user/data VLAN.





##### **Trunk Configuration**



The switch-to-switch links are configured as 802.1Q trunks.



The trunks use VLAN 999 as the native VLAN and allow the required VLANs:



switchport mode trunk

switchport trunk native vlan 999

switchport trunk allowed vlan 10,20,999





##### **STP Configuration**



Rapid PVST+ is enabled on the switches:



spanning-tree mode rapid-pvst



S1 is configured as the preferred Root Bridge for VLAN 10:



spanning-tree vlan 10 root primary



This allows the STP topology to be intentionally controlled instead of relying on automatic Root Bridge election.





##### **Edge Port Security**



PortFast and BPDU Guard are configured on ports connected to end devices.



spanning-tree portfast

spanning-tree bpduguard enable



**PortFast**



PortFast allows an access port connected to an end device to transition to the forwarding state quickly.





**BPDU Guard**



BPDU Guard protects an edge port by preventing an unexpected switch from being connected to the port and participating in STP.





##### **Verification**



The following commands are used to verify the configuration:



show vlan brief

show interfaces trunk

show spanning-tree

show spanning-tree vlan 10

show spanning-tree root

show running-config

STP Verification



The STP output is checked to identify:



* Root Bridge
* Root Port
* Designated Ports
* Alternate Ports
* STP path cost
* Forwarding and non-forwarding states





##### **What I Learned**



Through this lab, I learned how STP prevents Layer 2 loops by creating a loop-free logical topology while maintaining redundant physical links.



I also learned how to:



* Manually influence Root Bridge election
* Understand STP port roles
* Configure Rapid PVST+
* Configure trunk links
* Use a dedicated native VLAN
* Verify STP using Cisco IOS commands
* Apply PortFast and BPDU Guard to edge ports
* Identify redundant paths and understand why STP blocks them

