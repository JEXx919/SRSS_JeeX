## Descripción
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.

To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!

Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.cylabacademy.net/library/5806be215fe6052652521da2db517d6e0e1ce81392cc30d4ed8967825b2cf94c/myNetworkTraffic.pcap) and try to get the flag.


Filter your packets to narrow down your search.

Attacks were done in timely manner.

Time is essential
## solución 
```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ wget "https://challenge-files.cylabacademy.net/library/5806be215fe6052652521da2db517d6e0e1ce81392cc30d4ed8967825b2cf94c/myNetworkTraffic.pcap" -O myNetworkTraffic.pcap
--2026-10-17 23:52:30--  https://challenge-files.cylabacademy.net/library/5806be215fe6052652521da2db517d6e0e1ce81392cc30d4ed8967825b2cf94c/myNetworkTraffic.pcap
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.66, 13.226.187.22, 13.226.187.37, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.66|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1452 (1.4K) [application/octet-stream]
Saving to: ‘myNetworkTraffic.pcap’

myNetworkTraffic.pcap             100%[============================================================>]   1.42K  --.-KB/s    in 0.001s

2026-10-17 23:52:32 (1.03 MB/s) - ‘myNetworkTraffic.pcap’ saved [1452/1452]


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ tshark -r myNetworkTraffic.pcap -q -z io,phs
tshark: Error loading table 'TLS Decrypt': ssl_keys:5: File '/home/jeex/Webnet1/picopico.key' does not exist or access is denied.

===================================================================
Protocol Hierarchy Statistics
Filter:

frame                                    frames:22 bytes:1076
  raw                                    frames:22 bytes:1076
    ip                                   frames:22 bytes:1076
      tcp                                frames:22 bytes:1076
===================================================================

┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ tshark -r myNetworkTraffic.pcap -T fields -e frame.time_epoch -e tcp.payload | sort -n | cut -f2 | while read hex; do echo "$hex" | xxd -r -p | base64 -d 2>/dev/null; done
tshark: Error loading table 'TLS Decrypt': ssl_keys:5: File '/home/jeex/Webnet1/picopico.key' does not exist or access is denied.
_Ǽ���S�O��wV�k[s!WLj�#��+<���_�p�0�
                                   N/_���hfkD�������R�b�{���dacademy{1t_w4snt_th4t_34sy_tbh_4r_a55faeed}
```

```
academy{1t_w4snt_th4t_34sy_tbh_4r_a55faeed}
```
## notas adicionales

## referencias

