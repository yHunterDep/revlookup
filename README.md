# revlookup
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
./revlookup -h

usage: revlookup [-h] [-target TARGET] [-targets TARGETS]
                 [-cidr CIDR] [-o OUTPUT] [-s]

Revlookup 1.0 - HunterDep

options:
  -h, --help            show this help message and exit
  -target TARGET, --target TARGET
                        coloque o ip alvo, ex:
                        192.168.0.1
  -targets TARGETS, --targets TARGETS
                        coloque uma lista de ips, ex:
                        -targets ips.txt
  -cidr CIDR, --cidr CIDR
                        passe um Cidr, ex: 192.168.0.1/24
  -o OUTPUT, --output OUTPUT
                        salvar os resultados
  -s, --silent          tirar o banner
```

# Resolving an IP
```sh
./revlookup -target 140.82.113.31
./revlookup -target 87.248.98.39
```

# Solving a Cidr
```sh
./revlookup -cidr 87.248.98.0/24
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
