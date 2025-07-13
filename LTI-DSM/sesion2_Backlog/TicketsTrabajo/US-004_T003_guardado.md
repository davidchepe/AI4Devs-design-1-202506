# Título: API y Lógica de Guardado de Vacantes en Base de Datos

## Descripción: 
Desarrollar los endpoints de API y la lógica de persistencia para crear y guardar vacantes en la base de datos. Incluye la funcionalidad de guardado como borrador y la gestión de estados de vacante.

## Criterios de Aceptación:
- Endpoint POST /api/v1/jobs para crear nuevas vacantes
- Endpoint PUT /api/v1/jobs/{id} para actualizar borradores
- Guardado automático como borrador cada 30 segundos
- Asignación automática de tenant_id basado en usuario autenticado
- Generación de UUID único para cada vacante
- Timestamps de creación y modificación
- Soporte para guardado parcial (campos incompletos)
- Logging de acciones para auditoría

## Prioridad: 
Alta

## Estimación: 
2 puntos de historia

## Asignado a: 
Equipo de Backend

## Etiquetas: 
Backend, API, Base de Datos, Sprint 1

## Comentarios: 
Implementar transacciones para garantizar consistencia de datos. Considerar índices para optimizar consultas por tenant.

## Enlaces: 
- Esquema de base de datos Job
- Documentación OpenAPI
- Especificaciones multi-tenant

## Historial de Cambios:
- 13/07/2025: Creado por Product Manager
- 13/07/2025: Revisión de arquitectura por Backend Lead
