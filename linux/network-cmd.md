```bash
sudo tcpdump -nn -v -i eno1 -s 1500 -c 1 'ether proto 0x88cc'
```
The information that this provide you with is as follows

| name |  information |
| device host  | asw2-labr2c2-bry |
| device port  | GigabitEthernet1/0/17 |
| device software version |  Version 12.2(55)SE7 |
| device ip address | 10.10.10.1 |

```
tcpdump: listening on enp0s20f2, link-type EN10MB (Ethernet), capture size 1500 bytes
12:27:06.935371 LLDP, length 356
	Chassis ID TLV (1), length 7
	  Subtype MAC address (4): 38:1c:1a:3b:b8:80
	Port ID TLV (2), length 9
	  Subtype Interface Name (5): Gi1/0/17
	Time to Live TLV (3), length 2: TTL 120s
	System Name TLV (5), length 16: asw2-labr2c2-bry
	System Description TLV (6), length 248
	  Cisco IOS Software, C2960S Software (C2960S-UNIVERSALK9-M), Version 12.2(55)SE7, RELEASE SOFTWARE (fc1)\0x0aTechnical Support: http://www.cisco.com/techsupport\0x0aCopyright (c) 1986-2013 by Cisco Systems, Inc.\0x0aCompiled Mon 28-Jan-13 10:28 by prod_rel_team
	Port Description TLV (4), length 21: GigabitEthernet1/0/17
	System Capabilities TLV (7), length 4
	  System  Capabilities [Bridge, Router] (0x0014)
	  Enabled Capabilities [Bridge] (0x0004)
	Management Address TLV (8), length 12
	  Management Address length 5, AFI IPv4 (1): 10.10.10.1
	  System Port Number Interface Numbering (3): 0
	Organization specific TLV (127), length 6: OUI Ethernet bridged (0x0080c2)
	  Port VLAN Id Subtype (1)
	    port vlan id (PVID): 3267
	Organization specific TLV (127), length 9: OUI IEEE 802.3 Private (0x00120f)
	  MAC/PHY configuration/status Subtype (1)
	    autonegotiation [supported, enabled] (0x03)
	    PMD autoneg capability [10BASE-T hdx, 10BASE-T fdx, 100BASE-TX hdx, 100BASE-TX fdx, 1000BASE-T fdx] (0x6c01)
	    MAU type 1000BASET fdx (0x001e)
	End TLV (0), length 0
```


```bash
sudo tcpdump -nn -v -i eth0 -s 1500 -c 1 'ether[20:2] == 0x2000'
```
The information that is provide you with is as follows 
| name |  information |
| device host  | asw1-labr2c2-bry.ktt.net. |
| device port  | GigabitEthernet0/16 |
| device software version |  Version 12.2(25)SEE3 |
| device ip address | 10.10.10.1 |


```
07:54:25.713555 CDPv2, ttl: 180s, checksum: 0xc4d4 (unverified), length 372
	Device-ID (0x01), value length: 27 bytes: 'asw1-labr2c2-bry.ktt.net.'
	Version String (0x05), value length: 181 bytes:
	  Cisco IOS Software, C2960 Software (C2960-LANBASE-M), Version 12.2(25)SEE3, RELEASE SOFTWARE (fc2)
	  Copyright (c) 1986-2007 by Cisco Systems, Inc.
	  Compiled Thu 22-Feb-07 13:57 by myl
	Platform (0x06), value length: 22 bytes: 'cisco WS-C2960G-24TC-L'
	Address (0x02), value length: 13 bytes: IPv4 (1) 10.10.10.1
	Port-ID (0x03), value length: 19 bytes: 'GigabitEthernet0/16'
	Capability (0x04), value length: 4 bytes: (0x00000028): L2 Switch, IGMP snooping
	Protocol-Hello option (0x08), value length: 32 bytes:
	VTP Management Domain (0x09), value length: 0 bytes: ''
	Native VLAN ID (0x0a), value length: 2 bytes: 233
	Duplex (0x0b), value length: 1 byte: full
	AVVID trust bitmap (0x12), value length: 1 byte: 0x00
	AVVID untrusted ports CoS (0x13), value length: 1 byte: 0x00
	Management Addresses (0x16), value length: 13 bytes: IPv4 (1) 10.10.10.1

```
