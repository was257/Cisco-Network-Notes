

Router# show ip interface brife
```
  abd
```
Router# show ip interface brife


----------------------------
##Subnet

CIDR- Classless inter-domain Routing

VLSM- Variable Length Subnet Masks0


----------------------------
##VLan

`switch# show vlan brief`
> VLAN IS ON LAYER 2. SUBNET IS LAYER 3, Subnet can not stop layer 2 frame from flooding in lan.
> 
> IT SEPERATE LAN FOR 1.NETWORK PERFORMANT AND 2.NETWORK SECURITY (BROADCAST STORM)

```
switch(config)# vlan vlan_num //VLan configuration mode, also create VLan
switch(config-lvan)# name vlan_name
```

```
switch(config-if)# switchport mode access // set the switch port as an access port
switch(config-if)# switchport access vlan vlan_num // assign vlan_num to the port
```
>A access port is a switch port belongs to one VLan.Mostly connect to a host.

>A trunk port is one switch port(one interface) carries multiples VLans. Mostly connect to a switch or Sub-interfaces of Router(ROAS).
```
switch(config-if)# switchport trunk encapsulation dotlq // if switch supports both ISL and 802.1q,manualy set the encapsulation mode to 802.1q
switch(config-if)# switchport mode trunk // set the port as an trunk port
switch(config-if)# switchport trunk allow vlan vlan_id // allow a VLan to a given trunk port
switch(config-if)# switchport trunk native vlan vlan_id // for security , set a unused vlan as native VLan

switch# show interfaces trunk
```
>VLan Tag is used to identify VLan_id on FRAME. Frame sent throught trunk port will be tagged(with 802.1q untagged will be native VLAN).

>TRUNK Protocol: ISL(inter-switch link), 802.1Q(dot1q)

>802.1Q tag [source MAC add ][tpid(0x8100) 16bits | PCP 3bits | TCI 1bits | VID 12bits] [Type/Length]

>VID range 1-4094 , normal VID 1-1005 ,extended VID 1006-4094,
>
>802.1q has native VLAN VID=1, it will not be tagged.

### ROAS Router on a stick
```
router(config-if)# interface g0/0.10 //create sub-interface g0/0.10 on g0/0
router(config-subif)# encapsulation dot1q 10 //
router(config-subif)# ip address vlan_gateway vlan_masks //assign vlan gateway on router
router# show ip interface brief //sub-interfaces will be display as well
router# show ip route //sub-interfaces will be display as well(connected route and local route)
```
IN ROAS, Router will use sub-interface to route between VLans by tag(no Native VLan)

### SVI Switch Virtual Interfaces - LAYER3 SWITCH - Multilayer Switch
Instead of Router sub-interface.SVI configured ip address to be gateway of HOSTS.
```
router(config)# no interface g0/0.10 // delete sub-interface
router(config)# default interface g0/0 // reset interface to default settings
```
LAYERS SWTICH Will route the traffic inter VLans
```
switch(config)# ip routing // enable layer 3 routing on switch
switch(config-if)# no switchport //  set layer 2 switch port to layer 3 routed port
switch(config-if)# ip address ip_address ip_masks //
switch(config)# ip route 0.0.0.0 0.0.0.0 router_ip)_address // default route to router
switch# show interfaces status //

switch(config)# interface vlan10
switch(config-if)# ip address vlan_gateway_address masks
switch(config-if)# no shutdown // SVIs are shutdown by default
```
SVIs will replace trunk


----------------------------
## DTP Dynamic Trunking Protocol /VTP Vlan Trunking Protocol



----------------------------
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



