# &nbsp;			 **BUILD A NETWORK**



* ###  **How to enable the router**

##### &nbsp;       Router> **enable** 

##### &nbsp;	Router# **configure terminal**

##### &nbsp;	Router(config)# **hostname** Edge\_Router\_Backup

##### &nbsp;	Edge\_Router\_Backup(config)# **end**







* ### **Basic Switch configuration**

&nbsp;	

##### &nbsp;	Switch> **enable**

##### &nbsp;	Switch# **configure terminal**

##### &nbsp;	Switch(config)# **hostname** S1

##### &nbsp;	S1(config)# **enable secret** <key>

##### &nbsp;	S1(config)# **line console 0**

##### &nbsp;	S1(config-line)# **password** <password> 

##### &nbsp;	S1(config-line)# **login**

##### &nbsp;	S1(config-line)# **line vty 0 15**

##### &nbsp;	S1(config-line)# **password**  <password>

##### &nbsp;	S1(config-line)# **login**

##### &nbsp;	S1(config-line)# **exit**

##### &nbsp;	S1(config)# **service password-encryption**

##### &nbsp;	S1(config)# **banner motd** #No unauthorized access allowed!#

##### &nbsp;	S1(config)# **interface vlan1**

##### &nbsp;	S1(config-if)# **ip address** <ip address subnet mask>

##### &nbsp;	S1(config-if)# **no shutdown**

##### &nbsp;	S1(config-if)# **end**

##### &nbsp;	S1# **copy running-config startup-config**

##### &nbsp;	Destination filename \[startup-config]?

##### &nbsp;	Building configuration...

##### &nbsp;	\[OK]

##### &nbsp;	S1#







* ### **Basic Router Configuration Steps**



##### &nbsp;	Router> **enable**

##### &nbsp;	Router# **configure terminal**

##### &nbsp;	Enter configuration commands, one per line.

##### &nbsp;	End with CNTL/Z.

##### &nbsp;	Router(config)# **hostname** R1

##### &nbsp;	R1(config)#

##### &nbsp;	R1(config)# **enable secret** <key>

##### &nbsp;	R1(config)#

##### &nbsp;	R1(config)# **line console 0**

##### &nbsp;	R1(config-line)# **password** <password>

##### &nbsp;	R1(config-line)# **login**

##### &nbsp;	R1(config-line)# **exit**

##### &nbsp;	R1(config)#

##### &nbsp;	R1(config)# **line vty 0 4**

##### &nbsp;	R1(config-line)# **password** <password>

##### &nbsp;	R1(config-line)# **login**

##### &nbsp;	R1(config-line)# **transport input** ssh telnet

##### &nbsp;	R1(config-line)# **exit**

##### &nbsp;	R1(config)#

##### &nbsp;	R1(config)# **service password-encryption**

##### &nbsp;	R1(config)#

##### &nbsp;	R1(config)# **banner motd** #

##### &nbsp;	Enter TEXT message. End with the character '#'.

##### &nbsp;	\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

##### &nbsp;	WARNING: Unauthorized access is prohibited!

##### &nbsp;	\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

##### &nbsp;	R1(config)#

##### &nbsp;	R1# **copy running-config startup-config**

##### &nbsp;	Destination filename \[startup-config]?

##### &nbsp;	Building configuration...

##### &nbsp;	\[OK]

##### &nbsp;	R1#



