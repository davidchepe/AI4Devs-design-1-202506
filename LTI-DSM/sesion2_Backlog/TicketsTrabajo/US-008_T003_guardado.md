# Título: Persistencia y Gestión de Datos de Candidatos Parseados

## Descripción: 
Implementar la lógica de guardado de la información extraída de los CVs en la base de datos, incluyendo la creación/actualización de registros de candidatos, gestión de duplicados y almacenamiento del archivo original.

## Criterios de Aceptación:
- Creación de registros Candidate con datos parseados
- Actualización de candidatos existentes (detección por email)
- Almacenamiento seguro del archivo CV original
- Generación de UUID único para cada candidato
- Versionado de CVs cuando el candidato sube múltiples versiones
- Asociación automática a Applications según el contexto
- Transacciones atómicas para garantizar consistencia
- Índices optimizados para búsquedas por email y nombre

## Prioridad: 
Alta

## Estimación: 
3 puntos de historia

## Asignado a: 
Equipo de Backend

## Etiquetas: 
Backend, Base de Datos, Persistencia, Candidatos, Sprint 2

## Comentarios: 
Implementar estrategia de deduplicación robusta. Considerar el almacenamiento de archivos en cloud storage (S3, Azure Blob).

## Enlaces: 
- Esquema de base de datos Candidate
- Políticas de retención GDPR
- Especificaciones de almacenamiento de archivos

## Historial de Cambios:
- 13/07/2025: Creado por Product Manager
- 13/07/2025: Revisión de arquitectura de datos por Database Architect
