### **VLAN CONFIGURATION LAB**



##### **Overview**



This lab demonstrates how to configure and manage VLANs on Cisco switches using Cisco Packet Tracer.



##### **Objectives**



* Create VLANs on Cisco Switches
* Assign Swich ports to VLANs
* Configure a native VLAN
* Verify VLAN configurations



##### **VLAN Configuration**



|VLAN|Name|Purpose|
|-|-|-|
|10|VLAN-10|Grouping PC1 and PC3|
|20|VLAN-20|Grouping PC2 and PC4|
|999|UNUSED-NATIVE|Native/Unused VLAN|



##### **Devices**



* 1 x Cisco Switch 2960
* 4 x PC



##### **Configuration**



The Switch configurations are available in *configs* folder.



* *SWITCH 1.txt* - Switch 1 configuration



##### **Verification**



The following commands were used to verify the configuration:

show vlan brief

show interface status

show running-config



##### **RESULT**



The VLANS were successfully created and assigned to appropriate switch ports.



##### **TOOLS**



* Cisco Packet Tracer
* Cisco IOS

