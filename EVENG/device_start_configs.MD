```
# nxos (https://www.eve-ng.net/documentation/howto-s/107-howto-add-nx9k-switch)

boot nxos bootflash:nxos.7.0.3.I7.1.bin
!
username rick role priv-15 password snci2000
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

username bob privilege 15 secret abc123
!
interface Management1
   ip address 172.29.133.1/24
!
ip route 0.0.0.0/0 172.29.133.254
```
```
# iosl3
hostname vios
!
ip domain-name packetflow.local
!
crypto key generate rsa # 2048
ip ssh version 2
!
line vty 0 4
  transport input ssh
  login local
!
username bob privilege 15 secret abc123
!
interface GigabitEthernet0/0
 ip address 172.29.133.2 255.255.255.0
 no shut
!
ip route 0.0.0.0 0.0.0.0 172.29.133.254
```
# ref
https://www.eve-ng.net/documentation/howto-s/121-howto-add-images-from-virl

