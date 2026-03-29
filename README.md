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

# Resolving a file with IPS and Cidrs
The -targets argument needs a file with ips (CIDR or NORMAL) to work, example:
```sh
./revlookup -targets ips.txt
```

# Saving results
```sh
./revlookup -target 140.82.113.31 --output subs.txt
```

# Remove the Banner
```sh
./revlookup -target 140.82.113.31 --silent
```
