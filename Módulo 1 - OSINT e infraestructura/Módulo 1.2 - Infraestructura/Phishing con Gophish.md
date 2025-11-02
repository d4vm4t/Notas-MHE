# Tipos de phishing
- __Phishing Genérico__: Ataques masivos no dirigidos, buscando la mayor cantidad de víctimas posible.
- __Spear Phishing__: Ataques altamente dirigidos a individuos específicos, usando información personalizada (nombre, cargo, empresa).
- __Smishing__: Phishing a través de SMS (mensajes de texto).
- __Vishing__: Phishing a través de llamadas telefónicas (voz).

# Metodología de un Spear phishing
- __Reconocimiento (OSINT)__: Recopilación de información sobre el objetivo (emails, nombres, cargos, intereses, tecnologías).
- __Selección de Pretexto__: Crear una historia creíble que motive a la víctima a actuar (urgencia, curiosidad, miedo).
- __Creación de Artefactos__: Diseño de correos electrónicos convincentes y páginas de aterrizaje falsas (clones de sitios legítimos).
- __Envío de la Campaña__: Distribución masiva o dirigida de los correos/mensajes.
- __Explotación__: La víctima interactúa (hace clic, introduce credenciales, descarga archivo).
- __Post-Explotación__: El atacante utiliza la información obtenida (acceso a cuentas, instalación de malware).

# Requisitos par un ataque con Gophish
- Un servidor (Linux recomendado) con acceso a Internet y puertos abiertos (ej., 3333 para la interfaz web, 80/443 para la campaña, 25 para SMTP).
- Mailhog para smtp de pruebas: [https://github.com/mailhog/MailHog](https://github.com/mailhog/MailHog)
- Cuenta en mailgun (para pruebas con smtp real): [https://www.mailgun.com/](https://www.mailgun.com/)
- Cuenta en Google workspace (ofrecen una prueba gratuita): [https://workspace.google.com/](https://workspace.google.com/)
- Comprar un dominio (se puede crear gratis o usar una cuenta de correo en caso de que no sea gratis), en caso de comprar dominio un cifrado SSL.

Guía para crear un campaña con Gophish: [[Instalar gophish, mailhog y crear phishing básico]]
