```bash
sudo tcpdump -nn -v -i eno1 -s 1500 -c 1 'ether proto 0x88cc'

07:56:13.147276 LLDP, length 201
	Chassis ID TLV (1), length 7
	  Subtype MAC address (4): 00:90:0b:51:81:08
	Port ID TLV (2), length 7
	  Subtype MAC address (3): 00:90:0b:51:81:07
	Time to Live TLV (3), length 2: TTL 120s
	System Name TLV (5), length 4: ub11
	System Description TLV (6), length 93
	  Ubuntu 18.04.1 LTS Linux 4.15.0-42-generic #45-Ubuntu SMP Thu Nov 15 19:32:57 UTC 2018 x86_64
	System Capabilities TLV (7), length 4
	  System  Capabilities [Bridge, WLAN AP, Router, Station Only] (0x009c)
	  Enabled Capabilities [Bridge, Router] (0x0014)
	Management Address TLV (8), length 12
	  Management Address length 5, AFI IPv4 (1): 197.97.237.43
	  Interface Index Interface Numbering (2): 7
	Management Address TLV (8), length 24
	  Management Address length 17, AFI IPv6 (2): fe80::290:bff:fe51:8106
	  Interface Index Interface Numbering (2): 6
	Port Description TLV (4), length 6: enp2s0
	Organization specific TLV (127), length 9: OUI IEEE 802.3 Private (0x00120f)
	  Link aggregation Subtype (3)
	    aggregation status [supported], aggregation port ID 0
	Organization specific TLV (127), length 9: OUI IEEE 802.3 Private (0x00120f)
	  MAC/PHY configuration/status Subtype (1)
	    autonegotiation [supported, enabled] (0x03)
	    PMD autoneg capability [10BASE-T hdx, 10BASE-T fdx, 100BASE-TX hdx, 100BASE-TX fdx, Pause for fdx links, 1000BASE-T fdx] (0xec81)
	    MAU type 1000BASET fdx (0x001e)
	End TLV (0), length 0
1 packet captured
1 packet received by filter
0 packets dropped by kernel

```


```bash
sudo tcpdump -nn -v -i eth0 -s 1500 -c 1 'ether[20:2] == 0x2000'


07:54:25.713555 CDPv2, ttl: 180s, checksum: 0xc4d4 (unverified), length 372
	Device-ID (0x01), value length: 27 bytes: 'asw1-labr2c2-bry.isnet.net.'
	Version String (0x05), value length: 181 bytes:
	  Cisco IOS Software, C2960 Software (C2960-LANBASE-M), Version 12.2(25)SEE3, RELEASE SOFTWARE (fc2)
	  Copyright (c) 1986-2007 by Cisco Systems, Inc.
	  Compiled Thu 22-Feb-07 13:57 by myl
	Platform (0x06), value length: 22 bytes: 'cisco WS-C2960G-24TC-L'
	Address (0x02), value length: 13 bytes: IPv4 (1) 196.36.111.45
	Port-ID (0x03), value length: 19 bytes: 'GigabitEthernet0/16'
	Capability (0x04), value length: 4 bytes: (0x00000028): L2 Switch, IGMP snooping
	Protocol-Hello option (0x08), value length: 32 bytes:
	VTP Management Domain (0x09), value length: 0 bytes: ''
	Native VLAN ID (0x0a), value length: 2 bytes: 233
	Duplex (0x0b), value length: 1 byte: full
	AVVID trust bitmap (0x12), value length: 1 byte: 0x00
	AVVID untrusted ports CoS (0x13), value length: 1 byte: 0x00
	Management Addresses (0x16), value length: 13 bytes: IPv4 (1) 196.36.111.45

```
