Modelo: Claude 3.5 Sonnet

## Resumen General

Este documento contiene los prompts de la sesión 2 del proyecto LTI-DSM, enfocada en la creación del backlog de producto y análisis de trazabilidad entre casos de uso y user stories. El trabajo se basa en la documentación de requisitos generada en la sesión 1 y tiene como objetivo estructurar las épicas y historias de usuario para el desarrollo del ATS (Applicant Tracking System) LTI Hire.

**Prompt 1** establece el marco de trabajo para generar un roadmap detallado con épicas organizadas por milestones (M-1 MVP, M-2 Enhanced Features, M-3 Launch Ready) y user stories estructuradas siguiendo las mejores prácticas ágiles, incluyendo estimaciones en story points y criterios de aceptación detallados.

**Prompt 2** identifica una discrepancia importante entre los 3 casos de uso específicos del PRD (UC-01, UC-02, UC-03) y las 33 user stories más granulares generadas en el roadmap, cuestionando la alineación entre la documentación de requisitos y el backlog de desarrollo.

**Prompt 3** solicita un análisis de trazabilidad sin modificar el roadmap existente, resultando en un mapeo detallado que muestra cómo los 3 casos de uso del PRD se descomponen en 13 user stories directas (29.5% del roadmap) y se complementan con 20 user stories adicionales necesarias para infraestructura, cumplimiento legal y diferenciación competitiva.

**Prompt 4** formaliza el análisis de trazabilidad en un documento estructurado que incluye matrices de mapeo, análisis cuantitativo, justificación de user stories adicionales y recomendaciones para la implementación, estableciendo una base sólida para la planificación ágil del proyecto.

**Prompt 5** completa la documentación de la sesión actualizando el registro de prompts utilizados, manteniendo la trazabilidad de las decisiones de producto tomadas durante el proceso de análisis y diseño del backlog.

**Prompt 6** solicita la creación de tickets de trabajo detallados para tres user stories representativas (US-004, US-008, US-014) que cubren los casos de uso core del sistema, descomponiéndolas en tareas específicas con estructura formal de tickets ágiles.

**Prompt 7** profundiza en el análisis de la US-004 solicitando estimación de recursos, distribución de trabajo entre equipos (Frontend vs Backend) y análisis de dependencias para garantizar la finalización en un sprint.

**Prompt 8** solicita documentar el análisis de la US-004 y extenderlo a las US-008 y US-014, creando documentos de análisis previo que incluyen viabilidad, recursos necesarios, distribución de trabajo, gestión de riesgos y criterios de éxito para cada user story.

---

## Prompt1
Toma el rol de Product Manager y Business Analyst. Vamos a trabajar en Agile
Usamos como base los documentos generados en .\sesion1_DocumentoRequisitosProducto_PRD\ que serán nuestros documentos con los requisitos del producto
En la sesión de hoy sólo vamos a trabajar en .\sesion2_Baccklog\ que es donde vamos a generar las historias de usuario y el backlog de producto
Genera un documento "Roadmap.md" con las epicas y organiza las User Stories definidas en el PRD
Confirma que entiendes el cometido y no hagas nada sin consultarmelo
Genera también un documento "Prompts.md" donde actualices los prompts mas importantes que te vaya pidiendo. Añade a cada prompt el modelo usado. Al final del documento haz un resumen general del mismo. Tras el primer prompt, solo habrá un prompt un un resumen. Tras el segundo, dos promps y un resumen al final

## Prompt2
porque los casos de uso que había en LTI-DSM.md no coinciden con los que has propuesto en el Roadmap?

## Prompt3
Sin cambiar el Roadmap, dime la trazabilidad entre los casos de uso del PRD y las user stories que has generado

## Prompt4
Crea un documento explicando la trazabilidad entre los casos de uso del PRD y el nuevo Roadmap. Llama al documento "Trazabilidad_UCvsUS.md"

## Prompt5
Actualiza el documento Prompts.md con los nuevos prompts generados y actualiza el Resumen General

## Prompt6
Vamos a realizar las tres US. US-004, US-008 y US-014
Crea una carpeta debajo de .\sesion2_Backlog\ llamada TickesTrabajo. Dentro de esta, crea un fichero para cada uno de los tickets de trabajo de estas US. El nombre debe hacer referencia a la US que estamos detallando. Por ejemplo; US-004_T001_[descripcion corta], US-004_T002_[descripcion corta]

Quiero la siguiente estructura para los tickets de trabajo

Título: Implementación de Autenticación de Dos Factores (2FA)

Descripción: Añadir autenticación de dos factores para mejorar la seguridad del login de usuarios. Debe soportar aplicaciones de autenticación como Authenticator y mensajes SMS.

Criterios de Aceptación:

Los usuarios pueden seleccionar 2FA desde su perfil.
Soporte para Google Authenticator y SMS.
Los usuarios deben confirmar el dispositivo 2FA durante la configuración.
Prioridad: Alta

Estimación: 8 puntos de historia

Asignado a: Equipo de Backend

Etiquetas: Seguridad, Backend, Sprint 10

Comentarios: Verificar la compatibilidad con la base de usuarios internacionales para el envío de SMS.

Enlaces: Documento de Especificación de Requerimientos de Seguridad

Historial de Cambios:

01/10/2023: Creado por [nombre]
05/10/2023: Prioridad actualizada a Alta por [nombre]

Todos los tickets de trabajo deben seguir la misma estructura

Confirma las tareas a realizar antes de proceder

## Prompt7
Vamos a analizar en detalle los tickets de la US-004
Cuantos recursos estimas que necesitamos para garantizar que podemos terminar todo el trabajo en un único Sprint?
Como es el reparto de trabajo en % entre los diferentes equipos? FrontEnd y BackEnd? 
Cuales son las dependencias entre los diferentes tickets?

## Prompt8
Documenta este análisis dentro .\TicketsTrabajo\ con el nombre US-004_analisis_previo.md de forma que alfabeticamente sea el primer fichero de todos los que tienen el mismo nombre de usuario.

Después realiza el mismo análisis con el de las US-008 y US-014

Por ultimo actualiza el documento Prompts.md
