# Enumeração

Configuração inicial: `sudo nano /etc/hosts/`

## NMAP
Escaneamento de portas e serviços
```
nmap -sC -v -sV <ip>
```
## Fuzzing

<details>
  <summary>Path de Diretórios</summary>
  
  ```
  /usr/share/wordlists/dirbuster
  ```
  Txt disponíveis:
  
  - directory-list-2.3-medium.txt  
  - directory-list-lowercase-2.3-medium.txt
  - apache-user-enum-2.0.txt  
  - directory-list-1.0.txt  
  - directory-list-2.3-small.txt   
  - directory-list-lowercase-2.3-small.txt
</details>

### GOBUSTER
Busca de diretórios.
```
gobuster dir -u <ip> -w /usr/share/wordlists/dirb/common.txt
```
Busca de subdomínios
```
gobuster vhost -u <ip> -w wordlist.txt
```

### FFUF
Fuzzing para arquivos específicos:
```
ffuf -u <http://alvo.com/FUZZ> -w /usr/share/wordlists/dirb/big.txt -e .php,.txt,.html
```

### Outras Opções
Dirsearch: `dirsearch -u http://<ip>`
