We, Coloclue, have the intention to test the following features in a production environment.
- Large BGP communities (more details below)
- IPv6 on vMX on NFX250 (we have two NFX250's)

Customer Contact Details
------------------------
* Name: Network committee
* E-mail: routers@coloclue.net
* Telephone: N/A
* Company name: Netwerkvereniging Coloclue
* Job Title: N/A
* Address: Frans Duwaerstraat 34 / 1318 AC / Almere / The Netherlands

We'd be happy to provide a reference for marketing for a product contained in this beta program.

Additional information regarding our setup:
- Our network has multiple peering connections, it is likely AMS-IX will be connected to the vMX/NFX. The peers we have are listed on https://github.com/coloclue/peering/blob/master/peers.yaml
- We only have systems in production, currently based on Bird (a weather map can be found on https://sysadmin.coloclue.net/ )
- We have resources available to test the software
- We will inform you whenever we discover problems and think they might be related to the software/hardware

Test support for the action communities listed below:
```
remarks:        ACTION COMMUNITIES:
remarks:        ===================
remarks:        RFC 1997  | Large      | Meaning (Action)
remarks:        ----------+------------+-------------------------------------
remarks:        8283:50   | 8283:1:50  | Set LOCAL_PREF to 50 (default is 100)
remarks:        8283:150  | 8283:1:150 | Set LOCAL_PREF to 150 (default is 100)
remarks:        -         | 8283:2:0   | Prepend 8283 once to all eBGP peers
remarks:        -         | 8283:2:nnn | Prepend 8283 once to peer AS nnn
remarks:        -         | 8283:3:0   | Prepend 8283 twice to all eBGP peers
remarks:        -         | 8283:3:nnn | Prepend 8283 twice to peer AS nnn
remarks:        -         | 8283:4:0   | Do not export to eBGP peers
remarks:        -         | 8283:4:nnn | Do not export to peer AS nnn
remarks:        65535:0   | -          | G-SHUT [draft-ietf-grow-bgp-gshut]
remarks:        65535:666 | -          | BLACKHOLE [RFC 7999]
remarks:        ----------+------------+-------------------------------------
```
