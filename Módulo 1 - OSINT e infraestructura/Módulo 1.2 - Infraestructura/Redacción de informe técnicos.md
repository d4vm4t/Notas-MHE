# Tipos de informes
## Informe ejecutivo
- __Audiencia__: Alta dirección, personal sin conocimiento tecnico.
- __Foco__: Resumen de los riesgos de negocio, impacto general, tendencias, y recomendaciones de alto nivel.
- __Lenguaje__: No técnico, conciso, orientado al negocio.
- __Extensión__: Corto (suele ser una pagina o un párrafo).

## Informe técnico
- __Audiencia__: Equipos de TI, desarrolladores, administradores de sistemas, ingenieros de seguridad.
- __Foco__: Detalles técnicos de cada vulnerabilidad, pasos de reproducción, evidencia, y recomendaciones de remediación específicas.
- __Lenguaje__: Técnico, preciso, detallado.
- __Extensión__: Extenso (decenas o cientos de páginas).

# Elementos de un informe profesional
 - __Resumen Ejecutivo__: Visión general de los hallazgos clave y el riesgo general.
-  __Alcance y Metodología__: Qué se probó, cómo se hizo y qué herramientas se utilizaron.
 - __Hallazgos Detallados__: Descripción de cada vulnerabilidad.
	- __Impacto__: Consecuencias potenciales de la explotación.
	- __Evidencia__: Capturas de pantalla, logs, comandos de prueba.
	- __Recomendaciones de Remediación__: Pasos claros para corregir la vulnerabilidad.
	- __Nivel de Severidad__: Clasificación del riesgo.
 - Conclusiones Evaluación general y sugerencias.
 - __Anexos__: Información adicional (glosario, CVSS).

# Criterios de severidad
>El riesgo corporativo es el riesgo que de verdad importa a la hora de escribir ele informe, que vulnerabilidades podrías decir que equivalen a un impacto en negocio

- __Criticidad del Activo__: ¿Qué tan importante es el sistema o dato afectado para las operaciones de la empresa?
- __Impacto Financiero__: Pérdidas directas, multas, costos de recuperación.
- __Impacto Reputacional__: Daño a la imagen de la marca, pérdida de confianza de clientes.
- __Impacto Legal/Regulatorio__: Incumplimiento de normativas, litigios.
- __Impacto Operacional__: Interrupción de servicios, pérdida de productividad.
- __Diferencia con CVSS__: CVSS es técnico; el riesgo empresarial es contextual y específico de la organización.

# Estructura típica de un informe
- Resumen Ejecutivo
- Introducción
- Objetivos del Pentest
- Alcance
- Metodología
- Hallazgos
	- Vulnerabilidad 1 (Crítica)
	- Descripción
	- Impacto
	- Pasos de Reproducción
	- Evidencia
	- Recomendaciones
- Vulnerabilidad 2 (Alta)
- Conclusiones
- Recomendaciones Generales
- Anexos
- Glosario
- Puntuaciones CVSS completas
- Referencias

# Buenas Prácticas de Redacción: Claridad y Objetividad
__Claridad__:
- Usar lenguaje sencillo y directo.
- Evitar la jerga innecesaria o explicarla.
- Estructurar las frases y párrafos de forma lógica.

__Objetividad__:
- Basarse siempre en hechos y evidencias.
- Evitar opiniones personales o juicios de valor.
- Presentar los hallazgos de manera imparcial y verificable.

__Precisión__:
- Ser exacto en la descripción de las vulnerabilidades y sus impactos.
- Utilizar terminología técnica correcta.

__Concisidad__:
- Ir al grano, evitar el relleno.
- Cada palabra debe añadir valor.

# Errores Comunes al Redactar Informes
- __Falta de Claridad__: Lenguaje ambiguo o excesivamente técnico.
- __Información Incompleta__: Ausencia de pasos de reproducción, impacto o recomendaciones.
- __Exceso de Jerga__: No adaptar el lenguaje a la audiencia.
- __Falta de Evidencia__: No incluir capturas de pantalla o logs que demuestren el hallazgo.
- __Recomendaciones Vagas__: "Mejorar la seguridad" en lugar de "Implementar WAF".
- __Errores Gramaticales/Ortográficos__: Afectan la credibilidad.
- __No Priorizar__: Presentar todos los hallazgos con la misma importancia.
- __Falta de Resumen Ejecutivo__: No proporcionar una visión de alto nivel para la gerencia.