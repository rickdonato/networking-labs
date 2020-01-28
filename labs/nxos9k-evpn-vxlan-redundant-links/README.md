This topology is based upon -- nxos9k-evpn-vxlan -- with the following additions,
* 1 x port channel between leaf to spine (2 x member links, using unnumbered interfaces).
* Server's connected to 2 leafs for redundancy.
* Each server configured within a Bond (aka Bond0).
