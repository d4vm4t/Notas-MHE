- Tagas: #OSINT 
---
# ¿Qué es el OSINT?

>El OSINT (Open Source Intelligence) consiste en la inteligencia producida a partir de toda la información disponible públicamente.
- No requiere de ningún tipo de intrusión o método ilegal.
- Se basa en la recolección, procesamiento y análisis de datos de libre acceso.
---
# Objetivos del OSINT
- **Inteligencia de Amenazas:** Identificar y evaluar riesgos potenciales.
- **Due Diligence:** Investigación de individuos u organizaciones.
- **Investigaciones Digitales:** Apoyo a investigaciones forenses o criminales.
- **Conocimiento del Entorno:** Comprender mercados, competidores o el panorama social.
- **Seguridad Ofensiva (Red Teaming/Pentesting):** Preparación y reconocimiento de superficies de ataque, análisis de huella digital y creación de perfiles digitales.
- **Ingeniería Social:** Construcción de perfiles para campañas dirigidas.

## Ejemplos de uso
- Una empresa que investiga un posible socio comercial.
- Analistas de seguridad buscando vulnerabilidades en la exposición pública de una organización.
- Investigadores privados localizando a personas.

---

# Tipos de recopilación
En el OSINT existen dos tipos de recopilación: la **pasiva** y la **activa**. 
Su principal diferencia es el impacto y la actividad que se realiza en la págia

## Recopilación Pasiva
**Características:**
- No deja rastro directo en los sistemas del objetivo.
- Basada en información previamente publicada o almacenada en terceros.
- Generalmente más segura y menos riesgosa en términos de detección.

**Ejemplos:**
- Búsquedas en motores de búsqueda (Google, DuckDuckGo).
- Consulta de registros públicos (registros de empresas, propiedades).
- Revisión de perfiles de redes sociales abiertos.
- Lectura de noticias, blogs o foros públicos.
- Consulta de cachés de sitios web (Wayback Machine).

## Recopilación Activa
**Definición:**  
Recopilación de información que implica una interacción directa con el objetivo o su infraestructura, pero siempre dentro del marco de lo públicamente accesible.

**Características:**
- Puede dejar un rastro (logs, solicitudes DNS).
- Busca información “en vivo” o directamente del sistema público del objetivo.
- Requiere herramientas más específicas para la interacción.

**Ejemplos:**
- Consultas DNS directas (Nslookup, dig).
- Escaneo de puertos _para identificar servicios abiertos y su información pública_ (ej: banners de servicios web, versiones).
- Consulta de APIs públicas (ej: de servicios web, redes sociales).
- Interacción con sitios web para descubrir directorios o archivos públicos.
- Realizar whois queries para dominios.
---
# El ciclo de inteligencia
Una metodología buena de OSINT puede representar un éxito. Por lo tanto tener una metodología definida es muy importante.

El ciclo de inteligencia cuenta con 4 fases:
## 1. Preparación
Primero se debe definir claramente qué se quiere investigar, con qué alcance y bajo qué marco legal. Además de llevar a cabo las siguientes acciones clave:
- Establecer necesidades de inteligencia (qué información se busca y por qué).
- Definir indicadores clave (personas, dominios, IPs, organizaciones, palabras clave).
- Identificar fuentes abiertas potenciales (motores de búsqueda, redes sociales, foros...).
## 2. Recolección de información
En este paso se trata la obtención de datos de fuentes públicas (legalmente accesibles) que respondan a las preguntas definidas:
- Recopilar datos manual y automáticamente.
- Usar técnicas como Google Dorking, scraping o APIs públicas.
- Registrar fuente, fecha y hora de cada hallazgo.
- Mantener integridad de la información recolectada.
## 3.  Procesamiento de los datos
A continuación, se organiza y se depura la información recolectada para hacerla analizable. Obteniendo datos limpios y estructurados listos para la correlación y el análisis. 
- Se eliminan duplicados, datos irrelevantes o inconsistentes.
- Se estandarizar formatos (CSV, JSON, bases de datos, gráficos).
- Se clasificar información por tipo (infraestructura, humano, documento, OSINT técnico, etc.).
- Se preservan las evidencias mediante hashing y timestamp.
## 4. Análisis
Una vez tenemos los datos limpios y procesados se van a transformar en inteligencia, para descubrir patrones, relaciones y comportamientos. Como lo son:
- Correlacionar diferentes tipos de datos (por ejemplo, IP con un dominio o una persona).
- Identificar relaciones y patrones de comportamiento.
- Evaluar credibilidad y relevancia de cada hallazgo.
- Detectar vínculos con amenazas conocidas (malware, APT, fraudes, etc.).
## 5. Diseminación de resultados
Por último, se va a presentar la inteligencia de forma clara y útil para el público objetivo (técnico, estratégico o ejecutivo). Para ello:
- Se elaborarán informes técnicos, alertas tácticas o informes estratégicos.
- Se presentarán visualizaciones comprensibles (mapas de relación, gráficos, líneas de tiempo).
- Se compartirá la inteligencia con otros equipos (CERT, SOC, RRHH, legal) según el caso.
- Asegurar trazabilidad y cadena de custodia
---
# Aspectos legales y éticos
## Aspectos legales
- **Leyes de Protección de Datos y Privacidad:** (GDPR en Europa). No todo lo “público” puede ser recopilado y procesado libremente.
    - Información personal sensible.
    - Derecho al olvido, rectificación.

- **Términos de Servicio (ToS):**
    - El scraping automatizado de sitios web puede violar los ToS, incluso si la información es pública.
    - Uso de bots o scripts no autorizados.

- **Acceso No Autorizado:**
    - La recopilación de información pública no justifica el acceso a sistemas privados.

- **Propiedad Intelectual:**
    - Respetar derechos de autor sobre el contenido recopilado.

- **Difamación/Calumnia:**
    - Cuidado con la difusión de información no verificada o malinterpretada.

## Aspectos éticos
- **Privacidad:** Aunque la información sea pública, considerar la expectativa de privacidad del individuo. ¿Es ético usar cada pieza de información pública?

- **Contexto:** La información sacada de contexto puede ser engañosa, difamatoria o perjudicial.

- **Precisión:** Es una obligación ética verificar la exactitud y fiabilidad de la información antes de utilizarla o difundirla.

- **Sesgo:** Ser consciente de los propios sesgos cognitivos y de los posibles sesgos inherentes en las fuentes de información.

- **No Abusar:** No usar la información recopilada para hacer ingeniería social.

- **Impacto:** Considerar el impacto de su investigación y sus hallazgos en las personas o entidades involucradas.