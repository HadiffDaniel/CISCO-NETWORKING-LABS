### **TRUNK Configuration Lab**



##### **Overview**



This lab demonstrates how to configure, manage VLANs and implement trunk on Cisco switches using Cisco Packet Tracer.



##### **Objectives**



* Create VLANs on Cisco switches
* Assigned switch ports to VLANs
* Configure trunk ports
* Configure a native VLAN
* Verify VLAN and trunk configurations



##### **VLAN Configuration**



|VLAN|Name|Purpose|
|-|-|-|
|10|VLAN-10|Grouping PC1,PC2,PC5,PC6|
|20|VLAN-20|Grouping PC3,PC4,PC7,PC8|
|999|UNUSED-NATIVE|Native/unused VLAN|



##### **Devices**



* 2 x Cisco Switches 2960
* 8 x PC

##### 

##### **Files**



* TRUNK CONFIGURATIONS.pkt - Packet Tracer lab
* Topology.png             - Network topology
* Configs/SWITCH 1.txt     - Switch 1 2onfiguration
* Configs/SWITCH 2.txt     - Switch 2 configuration



##### **Verification**



The following commands were used to verify the configuration:



show vlan brief

show interface trunk

show interface status

show mac address-table

show running-config



##### **Result**



The VLANs were successfully created and assigned to the appropriate switch ports. 

Trunk connectivity and the native VLAN configuration were also verified.

##### 

##### **Tools**



* Cisco Packet Tracer
* Cisco IOS

##### **What I Learned**



* Configure trunk ports between Cisco switches to carry traffic from multiple VLANs.
* Learned how VLAN traffic can be extended between switches using trunk links.
* Configure and verify a native VLAN on trunk ports.
* Learned how to allow and manage multiple VLANs across a trunk connection.
* Learned how to verify trunk status, VLAN assignments, and MAC address learning using Cisco IOS commands.
* Gained hands-on experience implementing VLAN segmentation and inter-switch connectivity using Cisco Packet Tracer.
