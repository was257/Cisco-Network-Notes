

Router# show ip interface brife
Router# show ip interface brife


## OSPF V2

Router(config)# route ospf process_id
> create ospf process on router

Router(config-if)# ip ospf process_id area area_id
> active ospf process on interface

Router(config-route)# network ip_address wildcard_mask area area_number

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


##Serial connection
Router# show controllers interfaceid
> =DCE(Data Communication Equitment) DTE(Data Transmission Equitmnt)
Router(config-if)# clock rate rate_bps
> =on DCE side



