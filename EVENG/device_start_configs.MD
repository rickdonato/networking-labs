```
# nxos (https://www.eve-ng.net/documentation/howto-s/107-howto-add-nx9k-switch)

boot nxos bootflash:nxos.7.0.3.I7.1.bin
!
interface mgmt0
  vrf member management
  ip address 172.29.133.3/24
!
vrf context management
  ip route 0.0.0.0/0 172.29.133.254
```
```
# veos

interface Management1
   ip address 172.29.133.1/24
!
ip route 0.0.0.0/0 172.29.133.254
```
```
# iosl3

interface GigabitEthernet0/0
 ip address 172.29.133.2 255.255.255.0
 no shut

ip route 0.0.0.0 0.0.0.0 172.29.133.254
```
# ref
https://www.eve-ng.net/documentation/howto-s/121-howto-add-images-from-virl

