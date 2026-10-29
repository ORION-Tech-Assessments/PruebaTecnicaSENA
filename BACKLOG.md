# Backlog de ORION Maintenance Lite

## 1. Propósito

Este documento contiene las historias de usuario de la prueba para Aprendiz o Practicante SENA. Se debe priorizar el alcance obligatorio.

## HU-01: Registrar un activo

**Como** usuario de mantenimiento, **quiero** registrar un activo, **para** mantener un inventario básico.

### Datos mínimos
- Nombre.
- Tipo.
- Ubicación.
- Estado.

### Criterios de aceptación
1. Nombre, tipo y ubicación son obligatorios.
2. El sistema genera un identificador.
3. El sistema registra la fecha de creación.
4. El estado inicial es `Activo`, salvo selección explícita diferente.
5. Los errores de validación se muestran claramente.
6. El activo creado aparece en el listado.

**Prioridad:** Alta.

## HU-02: Consultar activos

**Como** usuario de mantenimiento, **quiero** consultar los activos registrados, **para** conocer los elementos disponibles.

### Criterios de aceptación
1. Mostrar identificador, nombre, tipo, ubicación y estado.
2. Permitir consultar el detalle.
3. Informar cuando no existan activos.
4. Informar cuando se consulte un activo inexistente.
5. Identificar claramente los activos inactivos.

**Prioridad:** Alta.

## HU-03: Editar un activo

**Como** usuario, **quiero** actualizar un activo, **para** mantener sus datos correctos.

### Criterios de aceptación
1. Editar nombre, tipo, ubicación y estado.
2. Validar nuevamente los campos obligatorios.
3. No modificar identificador ni fecha original de registro.
4. No actualizar activos inexistentes.

**Prioridad:** Media.

## HU-04: Desactivar un activo

**Como** usuario, **quiero** desactivar un activo, **para** indicar que ya no está disponible sin perder su información histórica.

### Criterios de aceptación
1. Cambiar el estado a `Inactivo`.
2. Conservar el activo en persistencia.
3. Conservar sus órdenes de trabajo.
4. Mantenerlo disponible para consulta.
5. No eliminar automáticamente información asociada.

**Prioridad:** Media.

## HU-05: Crear una orden de trabajo

**Como** usuario de mantenimiento, **quiero** crear una orden asociada a un activo, **para** registrar una actividad de mantenimiento.

### Datos mínimos
- Activo.
- Título.
- Descripción.
- Prioridad.

### Criterios de aceptación
1. El activo debe existir.
2. Título, descripción y prioridad son obligatorios.
3. Prioridades: `Baja`, `Media`, `Alta`.
4. Generar identificador.
5. Estado inicial `Pendiente`.
6. Registrar fecha de creación.
7. La nueva orden aparece en el listado.

**Prioridad:** Alta.

## HU-06: Consultar órdenes de trabajo

**Como** usuario, **quiero** consultar las órdenes, **para** conocer las actividades registradas.

### Criterios de aceptación
1. Mostrar identificador, título, activo, prioridad, estado y fecha.
2. Permitir consultar detalle.
3. El detalle muestra el activo asociado.
4. Informar si no existen órdenes.
5. Informar si una orden consultada no existe.

**Prioridad:** Alta.

## HU-07: Actualizar estado de una orden

**Como** usuario, **quiero** actualizar el estado de una orden, **para** reflejar su avance.

### Flujo permitido

`Pendiente -> En progreso -> Finalizada`

### Criterios de aceptación
1. Una orden nueva inicia en `Pendiente`.
2. `Pendiente` puede pasar a `En progreso`.
3. `En progreso` puede pasar a `Finalizada`.
4. `Finalizada` no puede regresar a estados anteriores.
5. No se permite `Pendiente -> Finalizada` directamente.
6. Los cambios inválidos muestran un mensaje.

**Prioridad:** Alta.

# Historias opcionales

## HU-08: Buscar activos
Buscar por nombre, tipo o ubicación. La búsqueda no modifica información y debe informar cuando no haya coincidencias.

## HU-09: Filtrar órdenes
Filtrar por estado o prioridad y permitir limpiar los filtros.

## HU-10: Indicadores básicos
Mostrar, por ejemplo, total de activos, activos activos/inactivos y órdenes por estado o prioridad alta.

## HU-11: Historial de estados
Registrar estado anterior, nuevo estado, fecha y opcionalmente una observación.

# Reglas de negocio generales

1. Cada activo y cada orden tienen identificador único.
2. Activo: nombre, tipo y ubicación obligatorios.
3. Orden: activo, título, descripción y prioridad obligatorios.
4. Una orden solo puede asociarse a un activo existente.
5. Toda orden inicia en `Pendiente`.
6. Flujo de estados: `Pendiente -> En progreso -> Finalizada`.
7. Una orden finalizada no regresa a estados anteriores.
8. Un activo desactivado conserva información y órdenes.
9. La aplicación debe validar la información antes de almacenarla.
10. Los errores deben expresarse mediante mensajes comprensibles.

# Orden recomendado de implementación

1. Modelo de activo.
2. Registro y consulta de activos.
3. Edición y desactivación.
4. Modelo de orden.
5. Creación y consulta de órdenes.
6. Cambio de estado.
7. Validaciones.
8. Pruebas.
9. Documentación.
10. Funcionalidades opcionales.

# Definición de terminado

Una historia se considera terminada cuando funciona, valida datos básicos, controla errores, persiste la información correspondiente, está disponible desde la interfaz, está versionada en Git y puede ser explicada por el candidato.
