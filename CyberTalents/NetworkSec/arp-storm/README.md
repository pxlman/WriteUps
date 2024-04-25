# Challenge Description

An attacker in the network is trying to poison the arp table of 11.0.0.100, the admin captured this PCAP.

Link Icon Link:
https://hubchallenges.s3-eu-west-1.amazonaws.com/Forensics/ARP+Storm.pcap

# Solving
First we want to check the pcap file for any interesting information
```
$ tshark -r ARP+Storm.pcap 
    1   0.000000 VMware_1e:1d:81 → Broadcast    ARP 42 Unknown ARP opcode 0x005a
    2   0.000442 VMware_1e:1d:81 → Broadcast    ARP 42 Unknown ARP opcode 0x006d
    3   0.000745 VMware_1e:1d:81 → Broadcast    ARP 42 Unknown ARP opcode 0x0078
    4   0.000994 VMware_1e:1d:81 → Broadcast    ARP 42 Unknown ARP opcode 0x0068
    5   0.001290 VMware_1e:1d:81 → Broadcast    ARP 42 Unknown ARP opcode 0x005a
    6   0.001567 VMware_1e:1d:81 → Broadcast    ARP 42 Unknown ARP opcode 0x0033
    7   0.001817 VMware_1e:1d:81 → Broadcast    ARP 42 Unknown ARP opcode 0x0074
    8   0.002152 VMware_1e:1d:81 → Broadcast    ARP 42 Unknown ARP opcode 0x006e
    9   0.002405 VMware_1e:1d:81 → Broadcast    ARP 42 Unknown ARP opcode 0x0063
...
...
...
```

So i can get this hexa code and translate it
```
$ tshark -r ARP+Storm.pcap | cut -d 'x' -f 2 | tr -d '\n' | xxd -r -p
ZmxhZ3tnckB0dWl0MHVzXzBwY09kZV8xc19BbHdAeXNfQTZ1U2VkX3QwX3AwMXMwbn0=
```

That looks like an base64 encode so let's decode it
```
$ tshark -r ARP+Storm.pcap | cut -d 'x' -f 2 | cut -c 3,4 | tr -d '\n' | xxd -r -p | base64 -d
flag{gr@tuit0us_0pcOde_1s_Alw@ys_A6uSed_t0_p01s0n}
```
## Flag
flag{gr@tuit0us_0pcOde_1s_Alw@ys_A6uSed_t0_p01s0n}
