# Lista de issues

**Proyecto integrador PR2 — María Eva Modarelli**  
Lista inicial vinculada al [cronograma y plan](CRONOGRAMA_Y_PLAN.md), al 6 de noviembre de 2026.

Estas son tareas propuestas para cargar en GitHub. **I01–I10 son referencias de este documento, no números reales de GitHub.** No se crearon issues automáticamente. Cada una se cargará en el repositorio donde se haga el cambio.

| Referencia | Tarea y repositorio | Criterio para terminarla | Estado |
| --- | --- | --- | --- |
| I01 | Crear bloqueo temporal — turnos | Validar agenda vigente, guardar proceso/propietario y vencimiento; probar conflictos y respuesta perdida sin reintentos ciegos | Pendiente |
| I02 | Confirmar inicialmente el bloqueo por REST — turnos | Confirmar el hold, persistir el resultado y tratar vencimiento o confirmación repetida | Pendiente; depende de I01 |
| I03 | Completar teléfono y resultados por Kafka — turnos | Enviar información adicional y procesar confirmación, rechazo, expiración y proceso inválido de forma idempotente | Pendiente; depende de I02 |
| I04 | Consultar y cancelar reservas propias — turnos | Probar con dos usuarios que ninguno puede ver ni cancelar reservas ajenas; cancelación repetida consistente | Pendiente; depende de I03 |
| I05 | Recuperar procesos interrumpidos — turnos | Recuperar estado después de reinicio, timeout o eventos duplicados/tardíos, sin crear reservas duplicadas ni reabrir estados finales | Pendiente; se prueba también durante I01–I04 |
| I06 | Cerrar búsqueda y filtro de disponibilidad — catálogo y coordinación con turnos | Acordar el contrato con el profesor y verificar los filtros obligatorios sin presentar agenda semanal como disponibilidad real | Pendiente |
| I07 | Completar Compose y seguridad de despliegue — backends | Arrancar ambos servicios y bases separadas; verificar configuración, JWT, transporte protegido y persistencia tras reinicio | Pendiente |
| I08 | Completar documentación y evidencias — documentación y READMEs técnicos | Pasos reproducibles y demostración de confirmación, expiración, cancelación, aislamiento e idempotencia coherentes con el código | Pendiente; cierre después de I01–I07 |
| I09 | Implementar cliente Android KMP — app-kmp | Registro/login, búsqueda, disponibilidad, reserva y cancelación desde la aplicación, sin credenciales técnicas | Pendiente; contratos backend necesarios |
| I10 | Preparar revisión de código — documentación y estudio | Explicar registro/JWT, disponibilidad y sincronización, mostrar pruebas y registrar dudas para la reunión antes del 21 | Pendiente; en paralelo al desarrollo |

## Uso de las issues

1. Al cargar una tarea en GitHub, agregar aquí su enlace y conservar la referencia del cronograma.
2. Escribir objetivo, alcance, criterios de aceptación y pruebas previstas. Si es demasiado grande, dividirla y relacionar las nuevas issues con la original.
3. Crear una rama desde `develop`, por ejemplo `feat/issue-N-crear-hold`, usando el número real de GitHub. Para un error, `fix/issue-N-descripcion`.
4. Abrir PR hacia `develop`, revisar el cambio y las pruebas; después integrar el bloque estable mediante PR de `develop` a `main`.
5. Distinguir **Pendiente**, **En curso**, **Integrado en develop** y **Disponible en main**. No dar por entregado lo que solo existe localmente. Con `main` como rama predeterminada, no asumir que un PR a `develop` cerrará automáticamente la issue; verificar el cierre al integrar en main.

Los avances ya implementados pueden registrarse con issues de organización o revisión que aclaren su situación real. No es necesario recrear artificialmente tareas ni fechas anteriores.

## Agregar inconvenientes o tareas nuevas

La lista está abierta. Si aparece un error o bloqueo:

- Crear una issue con un título concreto y el repositorio afectado.
- Describir qué se esperaba, qué pasó y cómo reproducirlo, sin publicar secretos.
- Relacionarla con la issue que bloquea, por ejemplo “bloquea I03”.
- Definir la prueba que permitirá confirmar la solución y asignar prioridad.
- Agregar una referencia nueva a esta lista y ajustar el cronograma si el inconveniente cambia las fechas.

No hace falta esperar una reunión para registrar un problema. La prioridad se revisa según su impacto en la tarea actual.

### Formato breve para una nueva issue

- **Título:** acción o problema concreto.
- **Repositorio:** dónde se hará el cambio.
- **Objetivo / problema:** resultado buscado y situación actual.
- **Aceptación:** qué debe cumplirse para terminar.
- **Prueba:** cómo se comprobará.
- **Relación:** qué tarea depende de ella o queda bloqueada.
- **Rama / PR / estado:** completar durante el trabajo.

[Volver al cronograma](CRONOGRAMA_Y_PLAN.md) · [Enunciado original](PROJECT_STATEMENT-v1.md) · [Referencia de integración original](INTEGRATION_REFERENCE-v2.md)
