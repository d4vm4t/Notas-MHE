# ¿Qué es un escáner de vulnerabilidades?
Un software automatizado diseñado para identificar debilidades de seguridad (vulnerabilidades) en redes y aplicaciones.

__Propósito__:
- Detectar configuraciones erróneas.
- Identificar software obsoleto o sin parches.
- Encontrar puertos y servicios expuestos.
- Reportar posibles puntos de entrada para actores.

__Diferencia en Pentesting__: Un escáner identifica vulnerabilidades. Un pentest intenta explotarlas para demostrar el riesgo real.

# ¿Cómo funciona un escáner?
Pasos Básicos:
1. __Reconocimiento__: Identifica los hosts activos en un rango de IP.
2. __Fingerprinting__: Determina el sistema operativo y los servicios en ejecución.
3. __Chequeo de Vulnerabilidades__: Compara las versiones de software y configuraciones con una base de datos de vulnerabilidades conocidas.
4. __Reporte__: Genera un informe detallado de los hallazgos.

__Base de Datos de Vulnerabilidades__: Los escáneres se actualizan constantemente con nuevas vulnerabilidades (plugins, NVD, etc.).

# CVE
__CVE (Common Vulnerabilities and Exposures)__: Es un diccionario de identificadores públicos para vulnerabilidades de seguridad conocidas.
- __Formato__: CVE-AAAA-NNNNN (Año-Número secuencial).
- __Ejemplo__: CVE-2017-0144 (EternalBlue, usado por WannaCry).

__NVD (National Vulnerability Database)__: Base de datos del gobierno de EE. UU. que complementa los CVEs con información adicional (descripciones, impactos, soluciones, puntuación CVSS).

>__Importancia en los scanners de vulnerabilidades__: Los escáneres utilizan bases de datos de CVEs para identificar si el software detectado es vulnerable a ataques conocidos.

# Nessus
Nessus dispone de varios tipos de escaneos:
- __Basic Network Scan__: Escaneo general de hosts y vulnerabilidades comunes.
- __Advanced Scan__: Permite personalizar completamente el escaneo (plugins, puertos, credenciales).
- __Web Application Test__: Enfocado en vulnerabilidades de aplicaciones web (OWASP Top 10).
- __Internal Network Scan__: Optimizado para redes internas.
- __Credentialed Patch Audit__: Verifica parches faltantes en sistemas con credenciales.
- __Malware Scan__: Detección de malware.
- __Compliance Scan__: Chequeos contra estándares de cumplimiento (CIS, PCI DSS).

# CVSS y Categorización de Hallazgos
__CVSS (Common Vulnerability Scoring System)__: Un estándar abierto para calificar la severidad de las vulnerabilidades.

Métricas Principales:
- __Base Score (Puntuación Base)__: Refleja las características intrínsecas de la vulnerabilidad (ej., acceso de red, complejidad del ataque, impacto en confidencialidad/integridad/disponibilidad).
- __Temporal Score (Puntuación Temporal)__: Ajusta la puntuación base según la disponibilidad de exploits, parches o mitigaciones.
- __Environmental Score (Puntuación Ambiental)__: Ajusta la puntuación según el contexto de la organización (ej., importancia del activo, controles de seguridad existentes).

>Nessus calcula y muestra la puntuación CVSS para cada vulnerabilidad, ayudando a los usuarios a comprender el riesgo de forma estandarizada.

# Consideraciones de red al escanear
- __Firewalls__: Pueden bloquear el tráfico de escaneo, impidiendo que Nessus vea los puertos y servicios.
- __IDS/IPS (Sistemas de Detección/Prevención de Intrusiones)__: Pueden detectar el escaneo como actividad maliciosa y bloquearlo o alertar.
- __Carga de Red__: Un escaneo intensivo puede generar una carga significativa en la red y los sistemas, especialmente en entornos de producción.
- __Importancia__: Planificar el escaneo con el equipo de red para evitar interrupciones o falsas alarmas.