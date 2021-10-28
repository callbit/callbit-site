---
layout: post
title:  "NMAP básico"
author: caubit
categories: [ cybersecuroty, captcha ]
image: assets/images/7.jpg
---
NMAP ("Network Mapper") é uma ferramenta free e opensouce para disconery de rede e auditoria de segurança. 

## Instalando NMAP
1. Atualizando pacotes do Linux
>`sudo apt-get update`
2. Install NMAP
>`sudo apt-get install nmap`
3. Verifique a versão 
>`nmap --version`

## Básico contra um host
> *nmap* ``1.1.1.1`` 
Ou você pode usar um endereço 
> nmap ``callbit.online``

## Scan contra uma porta especifica 
Um range de portas
> *nmap* -p ``1-65535`` ``1.1.1.1``
Uma serie de portas
> *nmap* -p ``80,443`` ``1.1.1.1``

## Scan de múltiplos IPs
> *nmap* ``1.1.1.1`` ``2.2.2.2``
Ips consecutivos
> *nmap* -p ``1.1.1.1,2,3,4``

## Scan nas portas mais populares
> *nmap* --top-ports ``20 192.168.1.106``

## Scan em range de IP
> *nmap* -p ``8.8.8.0/28`` ou *nmap* ``8.8.8.1-14``

## Scan agressivo
> *nmap* -A ``8.8.8.0``

## Scan máquinas ativas
> *nmap* -sP ``8.8.8.0``

## Scan agressivo
> *nmap* -sL ``8.8.8.0``

## Scan obter o SO
> *nmap* -O ``8.8.8.0``

## Scan com scripts básicos
> *nmap*  -Pn --script vuln ``8.8.8.0``

