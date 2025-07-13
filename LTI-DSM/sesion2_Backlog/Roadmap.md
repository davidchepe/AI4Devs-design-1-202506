# LTI Hire - Product Roadmap

> Roadmap de producto organizado por épicas y user stories  
> Fecha: Julio 2025  
> Product Manager: [Nombre]  
> Business Analyst: [Nombre]

---

## 📋 Visión del Producto

**LTI Hire** es un ATS (Applicant Tracking System) SaaS multi-tenant enfocado al mercado europeo, 100% conforme con GDPR, que utiliza IA para matching semántico y reduce el time-to-hire en más del 30%.

---

## 🗺️ Roadmap por Milestones

### 🎯 M-1: MVP (Milestone 1)
**Objetivo**: Lanzar funcionalidad core del ATS con matching semántico básico  
**Duración**: 4 sprints (8 semanas)  
**Fecha objetivo**: [Definir]

### 🎯 M-2: Enhanced Features (Milestone 2)
**Objetivo**: Integrar herramientas de productividad y reporting  
**Duración**: 3 sprints (6 semanas)  
**Fecha objetivo**: [Definir]

### 🎯 M-3: Launch Ready (Milestone 3)
**Objetivo**: Producto listo para lanzamiento comercial  
**Duración**: 2 sprints (4 semanas)  
**Fecha objetivo**: [Definir]

---

## 📚 Épicas y User Stories

### 🏗️ ÉPICA 1: Gestión de Usuarios y Autenticación
**Milestone**: M-1  
**Valor de negocio**: Permitir acceso seguro y control de roles en entorno multi-tenant

#### User Stories:

**US-001: Registro de Empresa (Tenant)**
- **Como** administrador de LTI
- **Quiero** poder registrar nuevas empresas en el sistema
- **Para** que puedan usar el ATS de forma independiente
- **Criterios de aceptación**:
  - Crear tenant con datos básicos (nombre, dominio, plan)
  - Configurar branding básico (logo, colores)
  - Enviar credenciales de administrador inicial
- **Estimación**: 8 SP
- **Prioridad**: Alta

**US-002: Autenticación de Usuarios**
- **Como** usuario del sistema
- **Quiero** poder autenticarme de forma segura
- **Para** acceder a las funcionalidades según mi rol
- **Criterios de aceptación**:
  - Login con email/password
  - Recuperación de contraseña
  - Sesiones seguras con JWT
  - Logout funcional
- **Estimación**: 5 SP
- **Prioridad**: Alta

**US-003: Gestión de Roles y Permisos (RBAC)**
- **Como** administrador de empresa
- **Quiero** asignar roles a mis usuarios
- **Para** controlar qué funcionalidades puede usar cada uno
- **Criterios de aceptación**:
  - Roles: Recruiter, Hiring Manager, Admin, External Agency
  - Permisos granulares por funcionalidad
  - Interfaz de gestión de usuarios
- **Estimación**: 13 SP
- **Prioridad**: Alta

---

### 🏗️ ÉPICA 2: Gestión de Vacantes
**Milestone**: M-1  
**Valor de negocio**: Permitir crear, gestionar y publicar ofertas de trabajo

#### User Stories:

**US-004: Crear Vacante**
- **Como** recruiter
- **Quiero** crear una nueva vacante
- **Para** iniciar un proceso de selección
- **Criterios de aceptación**:
  - Formulario con campos obligatorios (título, descripción, ubicación, salario)
  - Validación de datos
  - Guardado como borrador
  - Tags y categorización
- **Estimación**: 8 SP
- **Prioridad**: Alta

**US-005: Publicar Vacante**
- **Como** recruiter
- **Quiero** publicar una vacante
- **Para** que los candidatos puedan aplicar
- **Criterios de aceptación**:
  - Publicación en portal propio
  - URL pública de la vacante
  - Estado "Activo/Inactivo"
  - Fecha de expiración
- **Estimación**: 5 SP
- **Prioridad**: Alta

**US-006: Gestionar Vacantes**
- **Como** recruiter
- **Quiero** ver y editar mis vacantes
- **Para** mantenerlas actualizadas
- **Criterios de aceptación**:
  - Lista de vacantes con filtros
  - Editar vacante existente
  - Duplicar vacante
  - Archivar/eliminar vacante
- **Estimación**: 8 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 3: Gestión de Candidaturas
**Milestone**: M-1  
**Valor de negocio**: Recibir, procesar y gestionar aplicaciones de candidatos

#### User Stories:

**US-007: Aplicar a Vacante (Portal Candidato)**
- **Como** candidato
- **Quiero** aplicar a una vacante
- **Para** participar en el proceso de selección
- **Criterios de aceptación**:
  - Formulario de aplicación público
  - Subida de CV (PDF, DOC, DOCX)
  - Campos adicionales opcionales
  - Confirmación por email
- **Estimación**: 8 SP
- **Prioridad**: Alta

**US-008: Parseo Automático de CV**
- **Como** sistema
- **Quiero** extraer información del CV automáticamente
- **Para** facilitar la evaluación del candidato
- **Criterios de aceptación**:
  - Extracción de datos básicos (nombre, email, teléfono)
  - Identificación de skills y experiencia
  - Manejo de errores de parseo
  - Almacenamiento estructurado
- **Estimación**: 13 SP
- **Prioridad**: Alta

**US-009: Recepción por Email**
- **Como** candidato
- **Quiero** enviar mi CV por email
- **Para** aplicar de forma tradicional
- **Criterios de aceptación**:
  - Email dedicado por vacante
  - Procesamiento automático de adjuntos
  - Creación automática de candidatura
  - Notificación al recruiter
- **Estimación**: 8 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 4: Pipeline de Selección
**Milestone**: M-1  
**Valor de negocio**: Gestionar el flujo de candidatos a través del proceso de selección

#### User Stories:

**US-010: Pipeline Visual**
- **Como** recruiter
- **Quiero** ver el pipeline de candidatos visualmente
- **Para** entender el estado del proceso
- **Criterios de aceptación**:
  - Vista kanban con etapas configurables
  - Drag & drop para mover candidatos
  - Contadores por etapa
  - Etapas por defecto: Applied, Pre-screen, Interview, Offer, Hired, Rejected
- **Estimación**: 13 SP
- **Prioridad**: Alta

**US-011: Gestionar Estados de Candidatos**
- **Como** recruiter
- **Quiero** cambiar el estado de los candidatos
- **Para** reflejar su progreso en el proceso
- **Criterios de aceptación**:
  - Cambio de estado con motivo
  - Historial de cambios
  - Notificaciones automáticas al candidato
  - Campos adicionales por etapa
- **Estimación**: 8 SP
- **Prioridad**: Alta

**US-012: Notas y Comentarios**
- **Como** recruiter o hiring manager
- **Quiero** añadir notas sobre los candidatos
- **Para** documentar mi evaluación
- **Criterios de aceptación**:
  - Notas privadas y compartidas
  - Historial de comentarios
  - Menciones a otros usuarios
  - Adjuntar archivos
- **Estimación**: 5 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 5: Matching Semántico con IA
**Milestone**: M-1  
**Valor de negocio**: Utilizar IA para mejorar el matching entre vacantes y candidatos

#### User Stories:

**US-013: Búsqueda y Filtrado Básico**
- **Como** recruiter
- **Quiero** buscar y filtrar candidatos
- **Para** encontrar los más relevantes
- **Criterios de aceptación**:
  - Búsqueda por texto libre
  - Filtros por ubicación, experiencia, skills
  - Filtros knock-out configurables
  - Resultados paginados
- **Estimación**: 8 SP
- **Prioridad**: Alta

**US-014: Ranking Semántico**
- **Como** recruiter
- **Quiero** ver candidatos ordenados por relevancia
- **Para** priorizar mi revisión
- **Criterios de aceptación**:
  - Score de matching visible
  - Algoritmo basado en embeddings
  - Explicación del score (qué factores influyen)
  - Posibilidad de ajustar pesos
- **Estimación**: 21 SP
- **Prioridad**: Alta

**US-015: Shortlist Inteligente**
- **Como** recruiter
- **Quiero** crear shortlists automáticas
- **Para** acelerar la preselección
- **Criterios de aceptación**:
  - Sugerencia automática de top candidatos
  - Shortlist editable manualmente
  - Exportar shortlist
  - Notificar a hiring managers
- **Estimación**: 8 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 6: Portal del Candidato
**Milestone**: M-1  
**Valor de negocio**: Mejorar la experiencia del candidato y reducir consultas

#### User Stories:

**US-016: Timeline de Proceso**
- **Como** candidato
- **Quiero** ver el estado de mi aplicación
- **Para** conocer mi progreso en el proceso
- **Criterios de aceptación**:
  - Portal accesible con token único
  - Timeline visual del proceso
  - Estado actual claramente visible
  - Estimación de próximos pasos
- **Estimación**: 8 SP
- **Prioridad**: Media

**US-017: Biblioteca de Recursos (Vacía)**
- **Como** candidato
- **Quiero** acceder a recursos de mejora profesional
- **Para** desarrollar mis habilidades
- **Criterios de aceptación**:
  - Sección de biblioteca implementada
  - Mensaje de "próximamente"
  - Estructura preparada para contenido futuro
- **Estimación**: 3 SP
- **Prioridad**: Baja

---

### 🏗️ ÉPICA 7: Cumplimiento GDPR
**Milestone**: M-1  
**Valor de negocio**: Asegurar cumplimiento legal en mercado europeo

#### User Stories:

**US-018: Gestión de Consentimientos**
- **Como** candidato
- **Quiero** gestionar mis consentimientos de datos
- **Para** controlar el uso de mi información
- **Criterios de aceptación**:
  - Captura de consentimientos granulares
  - Posibilidad de revocar consentimientos
  - Log de consentimientos con timestamps
  - Formularios conformes GDPR
- **Estimación**: 13 SP
- **Prioridad**: Alta

**US-019: Exportar Datos Personales**
- **Como** candidato
- **Quiero** exportar mis datos personales
- **Para** ejercer mi derecho de portabilidad
- **Criterios de aceptación**:
  - Exportación en formato JSON estructurado
  - Incluir todos los datos asociados
  - Proceso automatizado
  - Entrega segura por email
- **Estimación**: 8 SP
- **Prioridad**: Media

**US-020: Derecho al Olvido**
- **Como** candidato
- **Quiero** solicitar la eliminación de mis datos
- **Para** ejercer mi derecho al olvido
- **Criterios de aceptación**:
  - Proceso de solicitud simple
  - Verificación de identidad
  - Eliminación completa de datos
  - Confirmación del proceso
- **Estimación**: 8 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 8: Internacionalización
**Milestone**: M-1  
**Valor de negocio**: Soportar múltiples idiomas del mercado europeo

#### User Stories:

**US-021: Soporte Multi-idioma**
- **Como** usuario
- **Quiero** usar la aplicación en mi idioma
- **Para** tener una mejor experiencia
- **Criterios de aceptación**:
  - Idiomas: ES, EN, FR, DE, IT
  - Cambio de idioma dinámico
  - Traducción de interfaz completa
  - Formatos locales (fechas, números)
- **Estimación**: 13 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 9: Branding y Personalización
**Milestone**: M-1  
**Valor de negocio**: Permitir personalización básica de marca por tenant

#### User Stories:

**US-022: Configuración de Branding**
- **Como** administrador de empresa
- **Quiero** personalizar la apariencia del sistema
- **Para** mantener mi identidad corporativa
- **Criterios de aceptación**:
  - Subir logo de empresa
  - Configurar colores primarios y secundarios
  - Vista previa en tiempo real
  - Aplicación en portal candidato
- **Estimación**: 8 SP
- **Prioridad**: Baja

---

## 🚀 MILESTONE 2 - Enhanced Features

### 🏗️ ÉPICA 10: Gestión de Entrevistas
**Milestone**: M-2  
**Valor de negocio**: Facilitar la programación y gestión de entrevistas

#### User Stories:

**US-023: Programar Entrevistas**
- **Como** recruiter
- **Quiero** programar entrevistas con candidatos
- **Para** avanzar en el proceso de selección
- **Criterios de aceptación**:
  - Integración con Google Calendar/Outlook
  - Invitaciones automáticas
  - Gestión de disponibilidad
  - Recordatorios automáticos
- **Estimación**: 13 SP
- **Prioridad**: Alta

**US-024: Módulo de Evaluaciones**
- **Como** hiring manager
- **Quiero** evaluar candidatos después de la entrevista
- **Para** documentar mi valoración
- **Criterios de aceptación**:
  - Formularios de evaluación configurables
  - Puntuaciones numéricas y comentarios
  - Consolidación de evaluaciones múltiples
  - Export de evaluaciones
- **Estimación**: 13 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 11: Comunicación y Plantillas
**Milestone**: M-2  
**Valor de negocio**: Automatizar y estandarizar comunicaciones

#### User Stories:

**US-025: Plantillas de Email**
- **Como** recruiter
- **Quiero** usar plantillas predefinidas para comunicarme
- **Para** ahorrar tiempo y mantener consistencia
- **Criterios de aceptación**:
  - Plantillas configurables por tenant
  - Variables dinámicas (nombre, vacante, etc.)
  - Editor WYSIWYG
  - Envío masivo de emails
- **Estimación**: 13 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 12: Reporting y Analytics
**Milestone**: M-2  
**Valor de negocio**: Proporcionar insights sobre el proceso de selección

#### User Stories:

**US-026: Dashboard de KPIs**
- **Como** recruiter o hiring manager
- **Quiero** ver métricas clave del proceso
- **Para** medir y optimizar mi rendimiento
- **Criterios de aceptación**:
  - Time-to-hire promedio
  - Tasas de conversión por etapa
  - Fuentes de candidatos más efectivas
  - Gráficos interactivos
- **Estimación**: 13 SP
- **Prioridad**: Media

**US-027: Reportes Exportables**
- **Como** hiring manager
- **Quiero** exportar reportes
- **Para** compartir con dirección
- **Criterios de aceptación**:
  - Export a PDF/Excel
  - Reportes parametrizables por fecha
  - Reportes por vacante o global
  - Programación de reportes automáticos
- **Estimación**: 8 SP
- **Prioridad**: Baja

---

### 🏗️ ÉPICA 13: Retención y Limpieza Automática
**Milestone**: M-2  
**Valor de negocio**: Cumplir con políticas de retención GDPR

#### User Stories:

**US-028: Políticas de Retención**
- **Como** sistema
- **Quiero** aplicar políticas de retención automáticas
- **Para** cumplir con GDPR sin intervención manual
- **Criterios de aceptación**:
  - Retención máxima 2 años post-proceso
  - Anonimización automática de datos expirados
  - Jobs de limpieza programados
  - Logs de acciones de retención
- **Estimación**: 13 SP
- **Prioridad**: Alta

---

## 🌟 MILESTONE 3 - Launch Ready

### 🏗️ ÉPICA 14: Integración Multicanal
**Milestone**: M-3  
**Valor de negocio**: Ampliar el alcance de publicación de vacantes

#### User Stories:

**US-029: Publicación en LinkedIn**
- **Como** recruiter
- **Quiero** publicar vacantes directamente en LinkedIn
- **Para** alcanzar más candidatos
- **Criterios de aceptación**:
  - Integración con LinkedIn Jobs API
  - Publicación con un clic
  - Sincronización de estado
  - Gestión de errores de API
- **Estimación**: 13 SP
- **Prioridad**: Alta

**US-030: Publicación en Indeed**
- **Como** recruiter
- **Quiero** publicar vacantes en Indeed
- **Para** maximizar la visibilidad
- **Criterios de aceptación**:
  - Integración con Indeed API
  - Mapeo de campos automático
  - Control de presupuesto
  - Estadísticas de rendimiento
- **Estimación**: 13 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 15: Portal de Agencias
**Milestone**: M-3  
**Valor de negocio**: Permitir colaboración con agencias externas

#### User Stories:

**US-031: Acceso para Agencias**
- **Como** agency recruiter
- **Quiero** acceder a vacantes asignadas
- **Para** colaborar en el proceso de selección
- **Criterios de aceptación**:
  - Rol de External Agency
  - Visibilidad limitada a vacantes asignadas
  - Funcionalidades restringidas
  - Facturación por uso
- **Estimación**: 21 SP
- **Prioridad**: Media

---

### 🏗️ ÉPICA 16: Recursos de Mejora Profesional
**Milestone**: M-3  
**Valor de negocio**: Diferenciarse ofreciendo valor adicional a candidatos

#### User Stories:

**US-032: Biblioteca de Contenidos**
- **Como** candidato
- **Quiero** acceder a recursos de mejora profesional
- **Para** desarrollar mis habilidades
- **Criterios de aceptación**:
  - Contenidos en video y PDF
  - Categorización por skills
  - Tracking de consumo
  - Recomendaciones personalizadas
- **Estimación**: 21 SP
- **Prioridad**: Baja

---

### 🏗️ ÉPICA 17: Firmas Electrónicas
**Milestone**: M-3  
**Valor de negocio**: Digitalizar completamente el proceso de contratación

#### User Stories:

**US-033: Integración DocuSign/Signaturit**
- **Como** recruiter
- **Quiero** enviar contratos para firma electrónica
- **Para** completar el proceso de contratación
- **Criterios de aceptación**:
  - Integración con servicios de firma
  - Templates de contratos
  - Tracking de estado de firma
  - Almacenamiento seguro de documentos firmados
- **Estimación**: 21 SP
- **Prioridad**: Baja

---

## 📊 Resumen de Estimación

### Por Milestone:
- **M-1 (MVP)**: ~210 Story Points
- **M-2 (Enhanced)**: ~80 Story Points  
- **M-3 (Launch)**: ~110 Story Points
- **TOTAL**: ~400 Story Points

### Por Prioridad:
- **Alta**: ~180 Story Points
- **Media**: ~150 Story Points
- **Baja**: ~70 Story Points

---

## 🎯 Criterios de Éxito por Milestone

### M-1 (MVP):
- [ ] Autenticación multi-tenant funcional
- [ ] CRUD completo de vacantes
- [ ] Recepción y parseo de candidaturas
- [ ] Pipeline visual operativo
- [ ] Matching semántico básico implementado
- [ ] Portal candidato con timeline
- [ ] Cumplimiento GDPR básico
- [ ] Soporte 5 idiomas europeos

### M-2 (Enhanced):
- [ ] Integración calendario funcional
- [ ] Sistema de evaluaciones completo
- [ ] Plantillas de comunicación
- [ ] Dashboard de KPIs operativo
- [ ] Retención automática implementada

### M-3 (Launch):
- [ ] Publicación multicanal funcional
- [ ] Portal agencias operativo
- [ ] Recursos profesionales disponibles
- [ ] Firmas electrónicas integradas
- [ ] SLA y monitoreo completo

---

## 📝 Notas y Dependencias

### Dependencias Técnicas:
- Setup inicial de infraestructura cloud (prerequisito M-1)
- Integración con servicios de IA para embeddings (prerequisito US-014)
- APIs externas (LinkedIn, Indeed) requieren aprobación y setup

### Riesgos Identificados:
- Complejidad del matching semántico puede impactar timeline M-1
- Integraciones externas pueden tener delays de aprobación
- Cumplimiento GDPR requiere validación legal continua

---

**Última actualización**: Julio 2025  
**Próxima revisión**: [Fecha]
