# Ejercicio de análisis y refinamiento

## Propósito

En un proyecto real, los requerimientos no siempre contienen toda la información necesaria. Este ejercicio busca conocer cómo identificas información faltante, formulas preguntas, documentas supuestos, reconoces riesgos y priorizas.

No existe una única respuesta correcta.

## Instrucciones

Para cada escenario:

1. Escribe preguntas adicionales.
2. Registra tus supuestos.
3. Explica la decisión que implementarás.
4. Identifica riesgos.

## Escenario 1: Activos duplicados

> El sistema debe permitir registrar activos y evitar registros duplicados.

Considera preguntas como: ¿cuándo son duplicados?, ¿el nombre es único?, ¿existe serial o código externo?, ¿se consideran activos inactivos?, ¿se bloquea o solo se advierte?

### Preguntas adicionales
```text
1.
2.
3.
```
### Supuestos
```text
1.
2.
3.
```
### Decisión de implementación
```text

```
### Riesgos
```text
1.
2.
```

## Escenario 2: Eliminación de activos

> El usuario debe poder eliminar un activo.

Un activo puede tener órdenes asociadas. ¿Debe eliminarse permanentemente?, ¿qué ocurre con sus órdenes?, ¿es preferible desactivarlo?, ¿debe pedirse confirmación?

### Preguntas adicionales
```text
1.
2.
3.
```
### Supuestos
```text
1.
2.
3.
```
### Decisión
```text

```
### Riesgos
```text
1.
2.
```

## Escenario 3: Órdenes simultáneas

> Se debe crear una orden de trabajo para realizar mantenimiento sobre un activo.

No se indica si un activo puede tener varias órdenes abiertas al mismo tiempo. ¿Se debe bloquear?, ¿advertir?, ¿qué estados se consideran abiertos?

### Preguntas adicionales
```text
1.
2.
3.
```
### Supuestos
```text
1.
2.
3.
```
### Decisión
```text

```
### Riesgos
```text
1.
2.
```

## Escenario 4: Flujo de estados

> Las órdenes pueden estar pendientes, en progreso o finalizadas.

Considera: ¿se puede finalizar directamente una pendiente?, ¿puede reabrirse?, ¿hace falta `Cancelada`?, ¿deben registrarse fechas de inicio/finalización?

### Preguntas adicionales
```text
1.
2.
3.
```
### Supuestos
```text
1.
2.
3.
```
### Decisión
```text

```
### Riesgos
```text
1.
2.
```

## Escenario 5: Priorización

> Las órdenes pueden tener prioridad baja, media o alta.

No se indica quién asigna la prioridad ni qué efecto tiene. ¿Se puede cambiar?, ¿alta aparece primero?, ¿requiere justificación?

### Preguntas adicionales
```text
1.
2.
3.
```
### Supuestos
```text
1.
2.
3.
```
### Decisión
```text

```
### Riesgos
```text
1.
2.
```

## Escenario 6: Responsables

> Las órdenes deben ser atendidas por personal de mantenimiento.

La versión obligatoria no solicita gestión de usuarios o cuadrillas. ¿Debe incluir responsable?, ¿uno o varios?, ¿forma parte de esta versión?

### Preguntas adicionales
```text
1.
2.
3.
```
### Supuestos
```text
1.
2.
3.
```
### Decisión
```text

```
### Riesgos
```text
1.
2.
```

# Priorización

Clasifica cada funcionalidad como Obligatoria, Importante, Opcional o Fuera del alcance.

| Funcionalidad | Clasificación | Justificación |
|---|---|---|
| Registrar activos |  |  |
| Listar activos |  |  |
| Editar activos |  |  |
| Desactivar activos |  |  |
| Crear órdenes |  |  |
| Consultar órdenes |  |  |
| Cambiar estado |  |  |
| Autenticación |  |  |
| Dashboard |  |  |
| Docker |  |  |
| Notificaciones |  |  |
| Aplicación móvil |  |  |
| Gestión de cuadrillas |  |  |
| Historial |  |  |
| Exportación Excel |  |  |
| Despliegue en nube |  |  |

# Diseño de la solución

## Tecnologías y motivo
```text

```
## Organización del código
```text

```
## Persistencia
```text

```
## Validaciones
```text

```
## Manejo de errores
```text

```
## Pruebas prioritarias
```text

```
## Riesgos de seguridad identificados
```text

```

# Plan de trabajo

| Paso | Actividad | Resultado esperado |
|---:|---|---|
| 1 |  |  |
| 2 |  |  |
| 3 |  |  |
| 4 |  |  |
| 5 |  |  |
| 6 |  |  |
| 7 |  |  |
| 8 |  |  |

# Resultado final

## Funcionalidades completadas
```text

```
## Funcionalidades pendientes
```text

```
## Principal dificultad encontrada
```text

```
## ¿Cómo resolviste los problemas encontrados?
```text

```
## ¿Qué mejorarías con más tiempo?
```text

```
## Tiempo aproximado dedicado
```text

```
## ¿Utilizaste herramientas de inteligencia artificial? ¿Para qué?
```text

```
## ¿Qué parte del código consideras más importante explicar?
```text

```

# Conocimientos sobre Microsoft 365 y Copilot

Como parte de la prueba técnica, responde las siguientes preguntas relacionadas con Microsoft 365, Copilot Studio y el desarrollo de aplicaciones basadas en agentes.

---

## 1. Microsoft 365 y Copilot

### ¿Qué es Microsoft 365 y qué recursos interoperan con Copilot?

### Respuesta

```text


```

---

## 2. Copilot Studio

### ¿Qué es Copilot Studio y qué ofrece?

### Respuesta

```text


```

---

## 3. Aplicaciones basadas en agentes

### ¿Qué mejores prácticas consideras para implementar, comprobar y evaluar aplicaciones con agentes?

### Respuesta

```text


```

---

## 4. Caso práctico: aplicación de inventario

> **Esta pregunta tiene un peso especial dentro de la evaluación.**

### Describa un caso de uso e implementación para una aplicación de inventario con información en varios archivos bajo el ambiente Microsoft 365 y Copilot.

### Respuesta

```text


```
