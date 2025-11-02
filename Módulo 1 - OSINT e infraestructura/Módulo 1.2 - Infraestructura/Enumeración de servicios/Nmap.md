>Nmap es una herramienta open source para el descubrimiento y auditoría de seguridad de redes.

# Sintaxis básica
```bash
nmap [tipo de escaneo] [opciones] [objetivo]

#Una única IP
nmap 192.168.1.1

#Rango de IPs
nmap 192.168.1.1-10

#Subred (CIDR)
nmap 192.168.1.0/24
```

# Tipos de escaneo
## SYN scan (-sS)
```bash
nmap -sS [objetivo]
```
- __Funcionamiento__: nmap envía un paquete SYN, y si recibe un SYN/ACK, sabe que el puerto está abierto. Luego envía un RST para cerrar la conexión sin completar el _handshake_ TCP.
- __Ventajas__: Rápido, sigiloso (no completa la conexión), menos probable que sea logueado por el objetivo.
- __Uso__: Es el escaneo por defecto para usuarios con privilegios.

## TCP connnect scan (-sT)
```bash
nmap -sT [objetivo]
```
- __Funcionamiento__: nmap completa un _handshake_ TCP de tres vías (SYN, SYN/ACK, ACK) con cada puerto
- __Ventajas__: funciona incluso sin privilegios de root.

## UDP scan (-sU)
```bash
nmap -sU [objetivo]
```
- __Funcionamiento__: Nmap envía paquetes UDP a los puertos y espera una respuesta. Si no hay respuesta (y no hay un ICMP 'Port Unreachable' filtrado), el puerto se considera abierto/filtrado. Si recibe 'Port Unreachable', el puerto está cerrado.
- __Ventajas__: necesario para identificar servicios basados en UDP.
- __Desventajas__: Muy lento, menos fiable (UDP no tiene confirmación de entrega), más difícil de interpretar.

# Descubrimiento de hosts
- __Ping Scan (-sn)__: solo descubre hosts acrtivos, sin escanear puertos
	```bash
	nmap -sn 192.168.1.0/24	
	```

- __No ping (-Pn)__: asume que todos los hosts están activos, salta la fase de ping. Útil solo si el objetivo bloquea ICMP.
	```
	nmap -Pn [objetivo]
	```

# Especificación de puertos
```bash
#Escaneo de puertos específicos
nmap -p80,443,22 [objetivo]

#Rango de puertos
nmap -p 1-1024 [objetivo]

#Todos los puertos
nmap -p- [objetivo]

#Puertos comunes
nmap [objetivo]
```

# Detección de servicios y versiones
```bash
nmap -sV [objetivo]

#Combinación común (SYN scan + detección de versiones)
nmap -sS -sV [objetivo] 
```
- __Funcionamiento__: Nmap envía intentos de conexion específicas a los puertos abiertos y analiza las respuestas (técnica de banner grabbing).
- __Importancia__: Conocer la versión exacta de un servicio permite buscar vulnerabilidades conocidas (CVEs) para esa versión.

# Uso de scripts NSE (Nmap Scripting Engine)
> NSE es un potente motor que permite a los usuarios escribir scripts (en lenguaje Lua) para automatizar una amplia variedad de tareas.

Categorías de scripts comunes:
- __auth__: Detección de credenciales por defecto, bypass de autenticación.
- __vuln__: Detección de vulnerabilidades específicas.
- __enum__: Enumeración de información (usuarios, recursos, DNS).
- __exploit__: Explotación de vulnerabilidades (uso con precaución).
- __brute__: Fuerza bruta de credenciales.

Uso:
```bash
#Ejecutar una categoría
nmap --script=vuln [objetivo]

#Ejecutar un script específico
nmap --script=http-enum [objetivo]

#Ejecutar todos los scripts predeterminados (lento)
nmap -sC [objetivo]
```

# Más usos de Nmap 
## Escaneo agresivo (-A)
Combina detección de SO (-O), detección de versiones (-sV), escaneo de scripts predeterminados (-sC) y traceroute.
```bash
nmap -A [objetivo]
```
- __Ventaja__: proporciona mucha información rápidamente
- __Desventaja__: muy ruidoso y fácil de detectar.

## Escaneo fragmentado
Divide los paquetes TCP en fragmentos más pequeños para intentar evadir algunos firewalls o IDS/IPS.
```bash
nmap -f [objetivo]
```

## "Evasión" de firewalls/IDS
```bash
#Añade datos aleatorios a los paquetes
--data-length <num>

#Envía paquetes con checksums TCP/UDP/IP inválidos
--badsum

#Especifica el puerto de origen
--source-port <port>

#Añade un retraso entre sondas para evitar detecciones por velocidad
--scan-delay <time>
```