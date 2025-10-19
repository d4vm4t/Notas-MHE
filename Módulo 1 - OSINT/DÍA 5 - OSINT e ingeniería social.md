- Tags: #OSINT 
---
# Perfilado de personas
- **Objetivo**: construir una imagen completa de un individuo basada en su huella digital pública.
- **Alcance**: desde datos básicos hasta intereses, conexiones y actividades online.
## Recolección de información basica
- **Datos clave**:
	-  Nombres y apellidos
	 - Seudónimos, alias o nombres de usuario frecuentes.
	 - Direcciones de correo electrónico (personales y profesionales).

 - Técnicas Iniciales:
	 - Búsquedas en motores de búsqueda (Google, DuckDuckGo) con diferentes combinaciones de nombres/alias.
	 - Consultas en bases de datos de personas públicas, como directorios profesionales.

## Técnicas de enumeración de nicknames (AKA)
- **WhatsMyName**: herramienta web para buscar un username.
- **Sherlock**: binario que busca un username en redes sociales.
- **Motores de búsqueda**: realizar la búsqueda usando Google dorking, en múltiples navegadores.
***Importancia**: un mismo alias puede conectar múltiples perfiles aparentemente no relacionados (eliminar falsos positivos)***

## Búsqueda de correos electrónicos
- Usar funciones de "recuperar contraseña" o "olvidé mi usuario" en sitios populares para ver si el email está vinculado a una cuenta.
- Usar paginas de filtraciones como `dehashed`.
- Probar con nicknames de cuentas

## Filtraciones de iformación
Con las filtraciones de información se busca contraseñas o información relevante del individuo, en paginas que recopilan filtraciones. Por ejemplo:
- **HaveIBeenPwned (HIBP)**: permite verificar si un correo electrónico ha aparecido en alguna brecha de datos pública.
- **Dehashed / IntelX**: plataformas que agregan grandes volúmenes de datos filtrados y permiten búsquedas más avanzadas.

## Recolección de huella digital en RRSS
- **Facebook**: información de perfil (si es pública), grupos, fotos, comentarios, eventos.
- **LinkedIn**: perfiles profesionales, historial laboral, educación, conexiones, habilidades.
- **Twitter/X**: tweets públicos, menciones, hashtags, seguidores, listas.
- **Instagram**: fotos, videos, historias (si son públicas), ubicación, hashtags.
- **Redes sociales geograficas**:
	- **China**: WeChat, Douyin
	- **Rusia**: VKontakte

## Búsqueda reversa de imágenes
- **Google Reverse Image Search**: subir una imagen para encontrar resultados visualmente similares.
- **PimEyes**: motor de búsqueda de reconocimiento facial que busca rostros similares en la web (uso controvertido, a menudo de pago).
- **Yandex Images**: ofrece mejores resultados y entrega muchas imagenes.

## Análisis de archivos internamente
Herramientas como **ExifTool** y **FotoForensics**.

## Análisis conceptual de imágenes
Consiste en un proceso muy técnico y analítico en el cual es necesario pensar fuera de la caja. En este tipo de análisis se examinan varios factores como:
- Arquitectura de los edificios
- Geografía del lugar
- Vegetación

## Motores de búsqueda
 Se pueden realizar búsquedas con Google dorking en los motores de búsqueda para recopilar información.

 Ejemplo: `site:linkedin.com "Nombre de la Empresa“`

## Uso de herramientas
En los procesos de OSINT también se hace uso de herramientas externas, como:
- **Maltego**:  herramienta que permite conectar diferentes entidades (personas, emails, dominios, IPs) y descubrir relaciones.
 - **Spiderfoot**: usada a nivel OSINT de infraestructura.

## Fuentes gubernamentales e industriales
Se tratan de registros oficiales, publicaciones legales, datos regulatorios y específicos de cada sector. Tiene gran importancia ya que proporcionan información altamente fiable y verificada sobre la estructura legal, finanzas y operaciones de una organización. 

Algunos ejemplos:
- Boletines oficiales
- Registro mercantiles
- Bases de datos de patentes
- Bases de datos de contratos y subvenciones:
	- **Portal de Transparencia (España)**: plataforma que publica información sobre la actividad del sector público, incluyendo contratos y subvenciones.
	- **BOE (Boletín Oficial del Estado)**: también publica convocatorias y resoluciones de contratos y subvenciones públicas.
	- **Adjudicaciones públicas**: registros de quién ganó qué contrato gubernamental

# Criterios de calidad de la información
- **Fiabilidad**: ¿Qué tan confiable es la fuente?.
- **Veracidad**: ¿Se puede verificar la información con otras fuentes independientes?
- **Actualidad:** ¿Cuándo fue publicada o actualizada la información? ¿Es todavía relevante?
- **Precisión:** ¿La información es exacta y sin ambigüedades?
- **Relevancia:** ¿La información contribuye directamente a los objetivos del perfilado?
- **Importancia:** La calidad de la inteligencia final depende directamente de la calidad de los datos de entrada



