# revlookup
Revlookup é uma ferramenta escrita em Python3 que realiza um DNS Reverso em IPs para a identificação de Subdomínios e novas aplicações

# Instalação e Uso
```sh
git clone https://github.com/yHunterDep/revlookup/
cd revlookup/
chmod +x revlookup
```

# Help do RevLookup
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

# Ultilizando o -target
```sh
./revlookup -target 140.82.113.31
./revlookup -target 87.248.98.39
```

# Ultilizando o -cidr
```sh
./revlookup -cidr 87.248.98.0/24
```

# Ultilizando o -targets
O argumento -targets precisa de um arquivo com ips (CIDR ou NORMAIS) para funcionar, exemplo:
```sh
./revlookup -targets ips.txt
```
