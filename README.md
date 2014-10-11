wifi
====

the script I'm using to manage wifi connections

Nota: this script uses wpa_supplicant and only handles wpa encryption.

Sample usage
============

```no-highlight
$ wifi add sample sample_essid
Adding sample (sample_essid)
thisisthekey
$ cat .wifi/sample 
# reading passphrase from stdin
network={
        ssid="sample_essid"
        #psk="thisisthekey"
        psk=53fef14b378242a3dfcfc0cb6444e47d4e46f67be8b0e2f87e7e5b4d765f5aa9
}
$ wifi sample
...
after few seconds
...
$ ping -c 1 lautre.net
PING lautre.net (80.67.160.91) 56(84) bytes of data.
64 bytes from 80.67.160.91: icmp_req=1 ttl=59 time=38.8 ms

--- lautre.net ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 38.828/38.828/38.828/0.000 ms
```
