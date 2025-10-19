- Tags: #OSINT 
---
# Técnicas de enumeración pasiva
## Información general
- **WHOIS de dominios**: realiza una consulta de bases de datos públicas a registradores, pudiendo conocer bastante información sobre la página web.
- **Inofrmación de DNS público**:
	- **crt.sh / Censys**: bases de datos de certificados SSL/TLS emitidos.
	- **DNS Dumpster**: herramienta web para visualizar la infraestructura DNS de un domino.
- **Información histórica de página web**: 
	- **Waybac Machine**: permite ver snapshots archivadas de sitios web a lo largo del tiempo. Al igual que **Archive.ph**
- **Motores de búsqueda pública**: 
	- **Shodan**: consulta de su base de datos de todo tipo de información, puertos abiertos y servicios, integración con API y “dorks”.
	- **ZoomEye**: similar a Shodan
	- **Censys**: alternativa a shodan, menos censura y consulta de certificados.
	- **FOFA**: Consulta de base de datos, censura mínima, pagina de china.

## Google Dorking
Ejemplos:
```
site:target.com filetype:pdf
site:target.com inurl:admin
site:target.com intitle:"Index of"
site:target.com intext:"password" | intext:"contraseña
inurl:wp-admin site:target.com
inurl:login.php intext:"failed login"
inurl:wp-admin
```

## Búsqueda en GitHub
En github y pastebin se puede buscar muchísima información, productos, código, API Keys…

## Análisis de sitios web
### Fingerprinting de tecnologías
- **Wappalyzer**: es una extensión de navegador que detecta las tecnologías de una página web visitada, analizando elementos del lado del cliente.
- **BuiltWith**: proporciona un perfil detallado de la pila tecnológica de un sitio web, a partir de sus bases de datos.
---
# Técnicas de enumeración activa
>  En este tipo de enumeración ya se consulta directamente al activo, genera mucha actividad y es muy ruidoso

## DNS
- **Comando 'host'**: `host www.Google.com`. Permite consultar registros MX, A, AAA, TXT...
- **Sublist3r**: `sublist3r -d kali.org -t 3 -e bing`
- **DNSrecon**: `dnsrecon -d megacorpone.com -t std`
- **DNSenum**: `dnsenum megacorpone.com`
- **nslookup**: `nslookup mail.megacorptwo.com`. Permite conocer la IP del dominio.
- **Gobuster y Wfuzz**: son herramienta de fuzzing que hacen fuerza bruta.
- **Amass y dig**

## Fingerprinting de tecnologías
- **Nmap**
- **Whatweb**
## URL públicas
Existen ficheros conocidos en paginas tales como `robots.txt`, `sitemap.xml`.