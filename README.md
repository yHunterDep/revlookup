# RevLookup
Revlookup is a tool written in Python3 that performs Reverse DNS on IPs to identify subdomains and new applications

# Installation and Use
```sh
git clone https://github.com/yHunterDep/revlookup/
cd revlookup/
pip3 install -r requirements.txt
chmod +x revlookup
```

# Help of RevLookup
```sh
$ ./revlookup -h

usage: revlookup [-h] [-target TARGET] [-targets TARGETS] [-cidr CIDR]
                 [-c CONCURRENT] [-o OUTPUT] [-s]

Revlookup 1.2 - HunterDep

options:
  -h, --help            show this help message and exit
  -target TARGET, --target TARGET
                        Target IP address or domain to perform reverse
                        lookup (e.g., 72.217.29.238 or google.com)
  -targets TARGETS, --targets TARGETS
                        File containing IPs, domains, or CIDR ranges for
                        reverse lookup (e.g., targets.txt)
  -cidr CIDR, --cidr CIDR
                        CIDR range to perform reverse lookup (e.g.,
                        87.248.98.0/24)
  -c CONCURRENT, --concurrent CONCURRENT
                        Set the number of concurrent threads to use during
                        scanning (default: 25)
  -o OUTPUT, --output OUTPUT
                        Output file to save results
  -s, --silent          Silent mode (disable banner)
```

# Resolving an IP
```sh
$ ./revlookup -target 140.82.113.31
 ____            _                _
|  _ \ _____   _| |    ___   ___ | | ___   _ _ __
| |_) / _ \ \ / / |   / _ \ / _ \| |/ / | | | '_ \
|  _ <  __/\ V /| |__| (_) | (_) |   <| |_| | |_) |
|_| \_\___| \_/ |_____\___/ \___/|_|\_\\__,_| .__/
                                            |_|

[>] Versão: 1.2
[$] Coded By HunterDep
[@] Github: https://github.com/yHunterDep

in-5.smtp.github.com
```

# Resolving a Domain (-target also)
```sh
$ ./revlookup -target yahoo.com
 ____            _                _
|  _ \ _____   _| |    ___   ___ | | ___   _ _ __
| |_) / _ \ \ / / |   / _ \ / _ \| |/ / | | | '_ \
|  _ <  __/\ V /| |__| (_) | (_) |   <| |_| | |_) |
|_| \_\___| \_/ |_____\___/ \___/|_|\_\\__,_| .__/
                                            |_|

[>] Versão: 1.2
[$] Coded By HunterDep
[@] Github: https://github.com/yHunterDep

media-router-fp74.prod.media.vip.gq1.yahoo.com
media-router-fp73.prod.media.vip.ne1.yahoo.com
media-router-fp73.prod.media.vip.bf1.yahoo.com
media-router-fp74.prod.media.vip.ne1.yahoo.com
media-router-fp74.prod.media.vip.bf1.yahoo.com
media-router-fp73.prod.media.vip.gq1.yahoo.com
```

# Solving a Cidr
```sh
$ ./revlookup -cidr 87.248.98.0/24
 ____            _                _
|  _ \ _____   _| |    ___   ___ | | ___   _ _ __
| |_) / _ \ \ / / |   / _ \ / _ \| |/ / | | | '_ \
|  _ <  __/\ V /| |__| (_) | (_) |   <| |_| | |_) |
|_| \_\___| \_/ |_____\___/ \___/|_|\_\\__,_| .__/
                                            |_|

[>] Versão: 1.2
[$] Coded By HunterDep
[@] Github: https://github.com/yHunterDep

vl-150.bas1-1-prd.ir2.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
ha2.vl-150.bas-1-prd.ir2.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
vl-150.bas2-1-prd.ir2.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
lsn4.ir2.yahoo.com
lsn3.ir2.yahoo.com
...
```

# Resolve a file containing domain names, IP addresses, or CIDRs, or all of them together.
Solving a file with subdomains
```sh
$ ./revlookup -targets yahoo_subdomains.txt
____            _                _
|  _ \ _____   _| |    ___   ___ | | ___   _ _ __
| |_) / _ \ \ / / |   / _ \ / _ \| |/ / | | | '_ \
|  _ <  __/\ V /| |__| (_) | (_) |   <| |_| | |_) |
|_| \_\___| \_/ |_____\___/ \___/|_|\_\\__,_| .__/
                                            |_|

[>] Versão: 1.2
[$] Coded By HunterDep
[@] Github: https://github.com/yHunterDep

media-router-fp74.prod.media.vip.ne1.yahoo.com
config.ydod.vip.a4e.yahoo.com
media-router-fp73.prod.media.vip.gq1.yahoo.com
media-router-fp74.prod.media.vip.bf1.yahoo.com
b31.f51.ymdb.a4e.yahoo.com
a44.f51.ymdb.a4e.yahoo.com
b21.f51.ymdb.a4e.yahoo.com
e1-ha.ycpi.cob.yahoo.com
ec2-98-86-247-55.compute-1.amazonaws.com
media-router-fp73.prod.media.vip.bf1.yahoo.com
a43.f51.ymdb.a4e.yahoo.com
b25.f51.ymdb.a4e.yahoo.com
b16.f51.ymdb.a4e.yahoo.com
b18.f51.ymdb.a4e.yahoo.com
b26.f51.ymdb.a4e.yahoo.com
b30.f51.ymdb.a4e.yahoo.com
e2-ha.ycpi.cob.yahoo.com
b24.f51.ymdb.a4e.yahoo.com
b29.f51.ymdb.a4e.yahoo.com
b27.f51.ymdb.a4e.yahoo.com
b23.f51.ymdb.a4e.yahoo.com
b19.f51.ymdb.a4e.yahoo.com
ec2-34-233-34-230.compute-1.amazonaws.com
smtp-yahoo.mail-prod1.omega.vip.bf1.yahoo.com
b15.f51.ymdb.a4e.yahoo.com
b22.f51.ymdb.a4e.yahoo.com
b28.f51.ymdb.a4e.yahoo.com
ec2-54-166-110-60.compute-1.amazonaws.com
a7de0457831fd11f7.awsglobalaccelerator.com
a7de0457831fd11f7.awsglobalaccelerator.com
ec2-44-195-146-171.compute-1.amazonaws.com
b32.f51.ymdb.a4e.yahoo.com
ats1.l7.search.vip.bf1.yahoo.com

...
```

Solving a file with cidr's
cidr_file.txt:
```
144.118.0.0/16
74.6.231.0/24
23.38.144.0/20
```
```sh
./revlookup -targets cidr_file.txt
 ____            _                _
|  _ \ _____   _| |    ___   ___ | | ___   _ _ __
| |_) / _ \ \ / / |   / _ \ / _ \| |/ / | | | '_ \
|  _ <  __/\ V /| |__| (_) | (_) |   <| |_| | |_) |
|_| \_\___| \_/ |_____\___/ \___/|_|\_\\__,_| .__/
                                            |_|

[>] Versão: 1.2
[$] Coded By HunterDep
[@] Github: https://github.com/yHunterDep

gw3-gi-0-1.noc.drexel.edu
gw4-gi-0-3-0.noc.drexel.edu
gw6-te-0-3-0-144-118-0-6.noc.drexel.edu
gw9-gi-0-2-144-118-0-9.noc.drexel.edu
gw12-te-7-1.noc.drexel.edu
gw13-te-7-1.noc.drexel.edu
gw12.noc.drexel.edu
gw6.noc.drexel.edu
gw4.noc.drexel.edu
...
media-router-fp71.canary.media.vip.ne1.yahoo.com
unknown.yahoo.com
vl-123.usw1-1-lbd.ne1.yahoo.com
vl-123.usw2-1-lbd.ne1.yahoo.com
media-router-fp73.prod.media.vip.ne1.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
vl-123.slb3-1-lbd.ne1.yahoo.com
ha1.vl-123.usw-1-lbd.ne1.yahoo.com
unknown.yahoo.com
unknown.yahoo.com
media-router-ui71.canary.media.vip.ne1.yahoo.com
...
```

# Saving results
```sh
./revlookup -target 140.82.113.31 --output subs.txt
```

# Remove the Banner
```sh
./revlookup -target 140.82.113.31 --silent
```
