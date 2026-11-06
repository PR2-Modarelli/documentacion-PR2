# Cronograma y plan de trabajo

**Proyecto integrador PR2 — María Eva Modarelli**  
Actualizado al 6 de noviembre de 2026.

## Objetivo

Presentar el avance del proyecto y las próximas etapas como referencia para el seguimiento con los profesores.

## Trabajo realizado

Durante octubre y los primeros días de noviembre se avanzó en la preparación del proyecto, el catálogo y la primera parte del servicio de turnos. El recorrido se organiza en estas etapas:

| Etapa | Trabajo realizado | Resultado |
| --- | --- | --- |
| Preparación del proyecto | Organización de repositorios y configuración de Java, Spring Boot, PostgreSQL y Docker | Entorno de trabajo preparado |
| Estructura del catálogo | Categorías, profesionales y horarios, relaciones, migraciones y persistencia | Catálogo almacenado en una base propia |
| Consulta e integración del catálogo | Descarga completa de datos de la cátedra, consultas locales, filtros y protección mediante JWT | Consulta del catálogo funcionando con datos de la cátedra |
| Actualización del catálogo | Integración con Kafka y Redis, control de versiones, eventos duplicados y recuperación | Sincronización automática implementada y actualizaciones comprobadas |
| Inicio del servicio de turnos | Conexión con el catálogo propio y consulta de ocupaciones de la cátedra | Cálculo de disponibilidad por profesional y fecha |
| Usuarios y autenticación | Registro, contraseñas protegidas, login con JWT y cuenta propia en una base independiente | Registro, login y disponibilidad probados en conjunto |
| Verificación del avance | Pruebas automatizadas y comprobaciones de integración | Base funcional para continuar con las reservas |

## Situación actual

El catálogo mantiene la información sincronizada con la cátedra. Turnos ya consulta ese catálogo, calcula horarios disponibles y permite registrar y autenticar usuarios. Se comprobó el recorrido de registro, login y consulta de disponibilidad con el JWT del usuario.

El siguiente bloque es crear un bloqueo temporal y conservar el proceso asociado al usuario que lo inicia. La confirmación, consulta y cancelación de reservas todavía están pendientes. También falta implementar Android KMP y completar las verificaciones de despliegue e integración.

## Próximos pasos y cronograma propuesto

Las fechas siguientes son objetivos de organización y se ajustarán según el avance, los inconvenientes y lo acordado con el profesor. Las referencias corresponden a la [lista de issues](ISSUES.md).

| Fecha objetivo | Trabajo previsto | Resultado esperado | Issues |
| --- | --- | --- | --- |
| 7–10 de noviembre | Persistir procesos de reserva y crear bloqueos temporales | Hold asociado al usuario, con vencimiento real y tratamiento de conflictos | I01 |
| 11–14 de noviembre | Confirmación inicial REST e intercambio de teléfono por Kafka | Procesamiento del resultado final sin duplicar ni retroceder estados | I02, I03 |
| 15–18 de noviembre | Consulta y cancelación de reservas propias | Cada usuario accede únicamente a sus procesos y reservas | I04 |
| 19–23 de noviembre | Recuperación de procesos pendientes y cierre de filtros | Pruebas de reinicios, timeouts, duplicados y contrato de búsqueda/disponibilidad | I05, I06 |
| 24–27 de noviembre | Ejecución conjunta y revisión de seguridad | Ambos backends y bases mediante Compose, configuración y transporte protegidos | I07 |
| 28 de noviembre en adelante, según fecha acordada | Correcciones, documentación y evidencias de backend | Demostración reproducible de los requisitos implementados | I08 |
| Según el plazo de presentación final que se acuerde | Cliente Android KMP | Flujo completo desde registro hasta reserva y cancelación | I09 |

Las pruebas y la documentación acompañarán cada etapa. El filtro de agenda existente no reemplaza el filtro de disponibilidad real; ese punto se completará dentro de la etapa de búsqueda.

## Próximo punto de seguimiento

Revisar el avance del bloqueo temporal: modelo del proceso de reserva, asociación con el usuario autenticado, vencimiento y tratamiento de conflictos. Como base se mantiene el recorrido de usuarios y disponibilidad que ya funciona.

Después de cada reunión se actualizarán avances, pendientes y objetivos del siguiente bloque. Si surge un inconveniente, se registrará una nueva issue y se ajustará el plan cuando sea necesario.

[Enunciado original](PROJECT_STATEMENT-v1.md) · [Referencia de integración original](INTEGRATION_REFERENCE-v2.md) · [Lista de issues](ISSUES.md)
