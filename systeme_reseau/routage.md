# Dans le Bash: 

-- tracert google.com -> affiche le routage

```
carmelina.napolitano@PC-DG-CAMPUS-22 MINGW64 ~
$ tracert google.com

D▒termination de l'itin▒raire vers google.com [216.58.209.238]
avec un maximum de 30 sauts▒:

  1    <1 ms    <1 ms    <1 ms  172.22.119.254
  2    <1 ms    <1 ms    <1 ms  172.22.0.254
  3     6 ms     6 ms     6 ms  212.99.63.254
  4    11 ms    14 ms     7 ms  172-1-1-88.lightspeed.hstntx.sbcglobal.net [172.                                                                                                                                                                                               1.1.88]
  5     *        *        *     D▒lai d'attente de la demande d▒pass▒.
  6     7 ms     7 ms     7 ms  172.17.15.1
  7     7 ms     9 ms    10 ms  89.227.215.254
  8     8 ms     8 ms     8 ms  92.103.121.247
  9     *        *        *     D▒lai d'attente de la demande d▒pass▒.
 10    17 ms    16 ms    16 ms  46.218.96.99
 11    16 ms    16 ms    16 ms  108.170.244.161
 12    16 ms    16 ms    16 ms  108.170.238.107
 13    16 ms    16 ms    16 ms  par10s29-in-f14.1e100.net [216.58.209.238]

Itin▒raire d▒termin▒.

```

-- Route PRINT-> toutes les règles de routage de mon pc


```
carmelina.napolitano@PC-DG-CAMPUS-22 MINGW64 ~
$ Route PRINT
===========================================================================
Liste d'Interfaces
 11...dc 4a 3e 6f d9 df ......Intel(R) Ethernet Connection (2) I219-LM
 14...0a 00 27 00 00 0e ......VirtualBox Host-Only Ethernet Adapter
  1...........................Software Loopback Interface 1
 12...00 00 00 00 00 00 00 e0 Microsoft ISATAP Adapter
 15...00 00 00 00 00 00 00 e0 Carte Microsoft ISATAP
===========================================================================

IPv4 Table de routage
===========================================================================
Itin▒raires actifs▒:
Destination r▒seau    Masque r▒seau  Adr. passerelle   Adr. interface M▒trique
          0.0.0.0          0.0.0.0   172.22.119.254   172.22.119.114     10
        127.0.0.0        255.0.0.0         On-link         127.0.0.1    306
        127.0.0.1  255.255.255.255         On-link         127.0.0.1    306
  127.255.255.255  255.255.255.255         On-link         127.0.0.1    306
     172.22.119.0    255.255.255.0         On-link    172.22.119.114    266
   172.22.119.114  255.255.255.255         On-link    172.22.119.114    266
   172.22.119.255  255.255.255.255         On-link    172.22.119.114    266
     192.168.56.0    255.255.255.0         On-link      192.168.56.1    266
     192.168.56.1  255.255.255.255         On-link      192.168.56.1    266
   192.168.56.255  255.255.255.255         On-link      192.168.56.1    266
        224.0.0.0        240.0.0.0         On-link         127.0.0.1    306
        224.0.0.0        240.0.0.0         On-link    172.22.119.114    266
        224.0.0.0        240.0.0.0         On-link      192.168.56.1    266
  255.255.255.255  255.255.255.255         On-link         127.0.0.1    306
  255.255.255.255  255.255.255.255         On-link    172.22.119.114    266
  255.255.255.255  255.255.255.255         On-link      192.168.56.1    266
===========================================================================
Itin▒raires persistants▒:
  Aucun

IPv6 Table de routage
===========================================================================
Itin▒raires actifs▒:
 If Metric Network Destination      Gateway
  1    306 ::1/128                  On-link
 14    266 fe80::/64                On-link
 14    266 fe80::fc8c:b4f2:4aef:1fa0/128
                                    On-link
  1    306 ff00::/8                 On-link
 14    266 ff00::/8                 On-link
===========================================================================
Itin▒raires persistants▒:
  Aucun

```

# Recherche Google:

who is ip -> traçage de l'ip (géoloc du serveur qui a cette ip
