# Trazabilidad: Casos de Uso PRD vs User Stories Roadmap

> Documento de trazabilidad entre los casos de uso definidos en el PRD y las user stories del roadmap de producto  
> Fecha: Julio 2025  
> Product Manager: [Nombre]  
> Business Analyst: [Nombre]

---

## 📋 Objetivo del Documento

Este documento establece la **trazabilidad completa** entre:
- Los **3 casos de uso** definidos en el PRD (LTI-DSM.md)
- Las **33 user stories** organizadas en el roadmap de producto

El objetivo es garantizar que todos los requisitos funcionales del PRD estén cubiertos en el backlog de desarrollo y identificar las funcionalidades adicionales necesarias para un producto comercialmente viable.

---

## 📖 Casos de Uso del PRD

### UC-01: Crear y publicar vacante
**Actor primario**: Recruiter  
**Flujo principal**: Crear vacante → Introducir datos → Seleccionar canales → Validar y publicar → Confirmar  
**Postcondición**: Vacante activa y visible en canales

### UC-02: Recibir y parsear candidaturas  
**Actor primario**: Recruiter (evento disparado por Candidate)  
**Flujo principal**: Candidato aplica → Sistema recibe → Parsea → Crea/actualiza Candidate → Crea Application → Envía confirmación  
**Postcondición**: Candidate y Application existen y están ligados

### UC-03: Filtrar y priorizar candidatos
**Actor primario**: Recruiter  
**Flujo principal**: Abrir listado → Aplicar filtros → Motor IA ranking → Seleccionar shortlist → Mover a Pre-screen → Notificar  
**Postcondición**: Lista priorizada y candidatos en siguiente etapa

---

## 🔗 Matriz de Trazabilidad

| **Caso de Uso** | **User Story** | **Épica** | **Milestone** | **Cobertura** | **Notas** |
|------------------|----------------|-----------|---------------|---------------|-----------|
| **UC-01** | US-004: Crear Vacante | ÉPICA 2 | M-1 | ✅ Core | Flujo principal paso 1-2 |
| **UC-01** | US-005: Publicar Vacante | ÉPICA 2 | M-1 | ✅ Core | Flujo principal paso 3-5 |
| **UC-01** | US-006: Gestionar Vacantes | ÉPICA 2 | M-1 | ✅ Extendido | Gestión post-creación |
| **UC-01** | US-029: Publicación LinkedIn | ÉPICA 14 | M-3 | ✅ Multicanal | Extensión canales |
| **UC-01** | US-030: Publicación Indeed | ÉPICA 14 | M-3 | ✅ Multicanal | Extensión canales |
| **UC-02** | US-007: Aplicar a Vacante | ÉPICA 3 | M-1 | ✅ Core | Flujo principal paso 1 |
| **UC-02** | US-008: Parseo Automático CV | ÉPICA 3 | M-1 | ✅ Core | Flujo principal paso 2-3 |
| **UC-02** | US-009: Recepción por Email | ÉPICA 3 | M-1 | ✅ Alternativo | Flujo alternativo |
| **UC-03** | US-010: Pipeline Visual | ÉPICA 4 | M-1 | ✅ Core | Visualización proceso |
| **UC-03** | US-011: Gestionar Estados | ÉPICA 4 | M-1 | ✅ Core | Flujo principal paso 5 |
| **UC-03** | US-013: Búsqueda/Filtrado | ÉPICA 5 | M-1 | ✅ Core | Flujo principal paso 2 |
| **UC-03** | US-014: Ranking Semántico | ÉPICA 5 | M-1 | ✅ Core | Flujo principal paso 3 |
| **UC-03** | US-015: Shortlist Inteligente | ÉPICA 5 | M-1 | ✅ Core | Flujo principal paso 4-6 |

---

## 📊 Análisis de Cobertura por Caso de Uso

### 🎯 UC-01: Crear y publicar vacante
**Cobertura**: ✅ **COMPLETA**

| **Aspecto del UC-01** | **User Story** | **Estado** |
|----------------------|----------------|------------|
| Crear módulo vacante | US-004 | ✅ Cubierto |
| Introducir datos obligatorios | US-004 | ✅ Cubierto |
| Validación de datos | US-004 | ✅ Cubierto |
| Seleccionar canales | US-005 | ✅ Cubierto |
| Publicación portal propio | US-005 | ✅ Cubierto |
| Confirmación y URL | US-005 | ✅ Cubierto |
| **Flujos alternativos** | | |
| Datos incompletos → errores | US-004 | ✅ Cubierto |
| Falla API → reintentar | US-029, US-030 | ✅ Cubierto |
| **Extensiones** | | |
| Gestión post-creación | US-006 | ✅ Añadido |
| Publicación LinkedIn | US-029 | ✅ Añadido |
| Publicación Indeed | US-030 | ✅ Añadido |

---

### 🎯 UC-02: Recibir y parsear candidaturas
**Cobertura**: ✅ **COMPLETA**

| **Aspecto del UC-02** | **User Story** | **Estado** |
|----------------------|----------------|------------|
| Candidato envía CV/formulario | US-007 | ✅ Cubierto |
| Sistema recibe archivo/JSON | US-007, US-009 | ✅ Cubierto |
| Parseo y normalización | US-008 | ✅ Cubierto |
| Crear/actualizar Candidate | US-008 | ✅ Cubierto |
| Crear Application "Applied" | US-008 | ✅ Cubierto |
| Correo confirmación | US-007 | ✅ Cubierto |
| **Flujos alternativos** | | |
| CV corrupto → almacenar sin parsear | US-008 | ✅ Cubierto |
| **Extensiones** | | |
| Recepción por email | US-009 | ✅ Añadido |

---

### 🎯 UC-03: Filtrar y priorizar candidatos
**Cobertura**: ✅ **COMPLETA**

| **Aspecto del UC-03** | **User Story** | **Estado** |
|----------------------|----------------|------------|
| Abrir listado candidatos | US-010 | ✅ Cubierto |
| Aplicar filtros knock-out | US-013 | ✅ Cubierto |
| Aplicar filtros skills | US-013 | ✅ Cubierto |
| Motor IA ranking por score | US-014 | ✅ Cubierto |
| Seleccionar shortlist | US-015 | ✅ Cubierto |
| Mover a etapa "Pre-screen" | US-011 | ✅ Cubierto |
| Notificar hiring managers | US-015 | ✅ Cubierto |
| **Flujos alternativos** | | |
| Sin resultados IA → orden cronológico | US-014 | ✅ Cubierto |
| **Extensiones** | | |
| Pipeline visual | US-010 | ✅ Añadido |
| Gestión estados completa | US-011 | ✅ Añadido |

---

## 🏗️ User Stories SIN Relación Directa con UC del PRD

### **ÉPICA 1: Gestión de Usuarios y Autenticación** (26 SP)
| **User Story** | **Justificación** | **Tipo** |
|----------------|------------------|----------|
| US-001: Registro Empresa | Prerequisito multi-tenant | Infraestructura |
| US-002: Autenticación | Prerequisito seguridad | Infraestructura |
| US-003: RBAC | Prerequisito control acceso | Infraestructura |

### **ÉPICA 6: Portal del Candidato** (11 SP)
| **User Story** | **Justificación** | **Tipo** |
|----------------|------------------|----------|
| US-016: Timeline Proceso | Diferenciador competitivo | Valor añadido |
| US-017: Biblioteca Recursos | Propuesta valor única | Valor añadido |

### **ÉPICA 7: Cumplimiento GDPR** (29 SP)
| **User Story** | **Justificación** | **Tipo** |
|----------------|------------------|----------|
| US-018: Gestión Consentimientos | Obligatorio mercado EU | Legal |
| US-019: Exportar Datos | Derecho portabilidad GDPR | Legal |
| US-020: Derecho Olvido | Derecho eliminación GDPR | Legal |

### **ÉPICA 8: Internacionalización** (13 SP)
| **User Story** | **Justificación** | **Tipo** |
|----------------|------------------|----------|
| US-021: Multi-idioma | Requisito mercado europeo | Técnico |

### **ÉPICA 9: Branding** (8 SP)
| **User Story** | **Justificación** | **Tipo** |
|----------------|------------------|----------|
| US-022: Configuración Branding | Requisito multi-tenant | Comercial |

### **Milestone 2: Enhanced Features** (80 SP)
| **Épicas** | **Justificación** | **Tipo** |
|------------|------------------|----------|
| ÉPICA 10-13 | Productividad y reporting | Evolución |

### **Milestone 3: Launch Features** (110 SP)
| **Épicas** | **Justificación** | **Tipo** |
|------------|------------------|----------|
| ÉPICA 15-17 | Características avanzadas | Evolución |

---

## 📈 Resumen Cuantitativo

### **Distribución por Relación con UC del PRD**
| **Categoría** | **User Stories** | **Story Points** | **Porcentaje** |
|---------------|------------------|------------------|----------------|
| **UC-01: Directas** | 3 US | 21 SP | 5.25% |
| **UC-01: Extendidas** | 2 US | 26 SP | 6.5% |
| **UC-02: Directas** | 3 US | 29 SP | 7.25% |
| **UC-03: Directas** | 5 US | 42 SP | 10.5% |
| **Infraestructura** | 3 US | 26 SP | 6.5% |
| **GDPR/Legal** | 3 US | 29 SP | 7.25% |
| **Valor Añadido** | 2 US | 11 SP | 2.75% |
| **Técnico/Comercial** | 2 US | 21 SP | 5.25% |
| **Evolución M-2/M-3** | 10 US | 195 SP | 48.75% |
| **TOTAL** | **33 US** | **400 SP** | **100%** |

### **Cobertura de UC del PRD**
- ✅ **UC-01**: 5 US (47 SP) - 11.75% del roadmap
- ✅ **UC-02**: 3 US (29 SP) - 7.25% del roadmap  
- ✅ **UC-03**: 5 US (42 SP) - 10.5% del roadmap
- **TOTAL UC PRD**: 13 US (118 SP) - **29.5% del roadmap**

---

## 🎯 Conclusiones y Recomendaciones

### ✅ **Fortalezas de la Trazabilidad**

1. **Cobertura Completa**: Los 3 UC del PRD están 100% cubiertos
2. **Detalle Granular**: Cada UC se descompone en múltiples US implementables
3. **Flujos Alternativos**: Se cubren los escenarios de error y casos edge
4. **Extensibilidad**: Se añaden capacidades que van más allá del MVP básico

### ⚠️ **Justificación de US Adicionales**

1. **Infraestructura (20 US - 70.5%)**: Necesaria para producto SaaS comercial
   - Multi-tenant, autenticación, GDPR, i18n son **prerequisitos obligatorios**
   - Sin estas funcionalidades, los UC del PRD no pueden ejecutarse en producción

2. **Diferenciación Competitiva**: Portal candidato y recursos profesionales
   - Alineado con propuesta de valor del PRD: "experiencia candidato superior"

3. **Evolución del Producto**: M-2 y M-3 añaden capacidades para escalabilidad comercial
   - Reporting, integraciones, agencias son necesarias para competir en el mercado

### 📋 **Recomendaciones**

1. **Priorización M-1**: Asegurar que los 13 US core de UC estén en las primeras iteraciones
2. **Validación Legal**: Revisar US de GDPR con equipo legal antes de implementar
3. **Feedback Temprano**: Implementar US-016 (Timeline) pronto para validar UX candidato
4. **Roadmap Flexible**: US de M-2/M-3 pueden reordenarse según feedback de mercado

---

## 📚 Referencias

- **Documento PRD**: `LTI-DSM.md` - Casos de uso UC-01, UC-02, UC-03
- **Roadmap Producto**: `Roadmap.md` - 33 User Stories organizadas por épicas
- **Diagramas UC**: `UC01_CreatePublishJob.png`, `UC02_ParseApplications.png`, `UC03_FilterPrioritize.png`

---

**Última actualización**: Julio 2025  
**Próxima revisión**: [Definir tras Sprint Planning]
