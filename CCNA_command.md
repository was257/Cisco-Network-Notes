

Router# show ip interface brife
```
  abd
```
Router# show ip interface brife


--
##Subnet
CIDR- Classless inter-domain Routing
VLSM- Variable Length Subnet Masks0


--
##VLan

`switch# show vlan brief`
> VLAN IS ON LAYER 2. SUBNET IS LAYER 3, Subnet can not stop layer 2 frame from flooding in lan.
> IT SEPERATE LAN FOR 1.NETWORK PERFORMANT AND 2.NETWORK SECURITY (BROADCAST STORM)

```
switch(config)# vlan vlan_num //VLan configuration mode, also create VLan
switch(config-lvan)# name vlan_name
```
```
switch(config-if)# switchport mode access // set the switch port as an access port
switch(config-if)# switchport access vlan vlan_num // assign vlan_num to the port
```
`switch(config)# switchport mode trunk`
>A access port is a switch port belongs to one VLan.Mostly connect to a host.
>A trunk port is one switch port(one interface) carries multiples VLans. Mostly connect to a switch.
>VLan Tag is used to identify VLan_id on FRAME. Frame sent throught trunk port will be taged.
>TRUNK Protocol: ISL(inter-switch link), 802.1Q(dot1q)
>802.1Q tag [source MAC add ][tpid(0x8100) 16bits | PCP 3bits | TCI 1bits | VID 12bits] [Type/Length]  
>vid range 1-4094


---
## OSPF V2

`Router(config)# route ospf process_id`
> create ospf process on router

Router(config-route)# shutdown
> shutownd

Router(config-if)# ip ospf process_id area area_id
> active ospf process on interface

Router(config-route)# network ip_address wildcard_mask area area_number
        abd
Router(config-route)# passive-interface interface-id

Router(config-route)# default information originate

Router# show ip route
> route codes:C=Connected,L=local,D=EIGRP,O=OSPF
> S*=Static Default Gateway

Router# show ip protocol
Routing protocol: 
Router(config-route)# router-id router id
Router(config-route)# distance ad(administrative distance)

Router# show ip ospf database   
> LSDB

Router# show ip ospf interface brief

## Serial connection
Router# show controllers interfaceid
> =DCE(Data Communication Equipment) DTE(Data Teriminal Equipment)
Router(config-if)# clock rate rate_bps
> =on DCE side



