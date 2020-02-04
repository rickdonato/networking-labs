# Multi Vendor 3 Tier Lab
Multi vendor lab based on a 3 tier topology.

## Key Points
* Vendors are Cisco, Juniper and Arista.
* Core is configured with OSPF.
* Aggregation NXOS's uses vPC.
* LACP downlinks from aggregation to each access switch.

## Caveats
When the aggrs come up the vPC peer link will be down. To resolve run the following on both aggrs, and check via `show int status`.

```
nxos-aggrx(config)# int e1/10,e1/11
nxos-aggrx(config-if-range)# shut
nxos-aggrx(config-if-range)# no shut
```


## Topology
![multivendor-3tier-topology](https://github.com/rickdonato/networking-labs/blob/master/labs/multivendor-ospf-vpc-3-tier/multivendor-3tier-topology.png)

## Credentials
* Core - `cisco/cisco`
* Aggr - `cisco/cisco`
* Access - `admin/admin123`


