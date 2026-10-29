# Prueba Técnica ORION Maintenance Lite

## Perfil: Aprendiz o Practicante SENA

## 1. Introducción

Bienvenido a la prueba técnica para aprendices y practicantes SENA del equipo de desarrollo de ORION.

El objetivo es conocer tus fundamentos de programación, capacidad para interpretar requerimientos, estructurar una solución y resolver problemas. No esperamos una aplicación con calidad productiva ni una arquitectura empresarial completa.

La prueba está basada en una versión simplificada de **ORION Maintenance**, orientada a la gestión de activos y órdenes de trabajo de mantenimiento.

## 2. Objetivo

Construir una aplicación web sencilla denominada **ORION Maintenance Lite** que permita:

1. Registrar activos.
2. Consultar activos.
3. Crear órdenes de trabajo asociadas a un activo.
4. Consultar órdenes de trabajo.
5. Actualizar el estado de una orden.
6. Conservar la información mediante algún mecanismo de persistencia.

## 3. Alcance obligatorio

### 3.1 Gestión de activos

La aplicación debe permitir registrar, listar, consultar, editar y desactivar activos.

Cada activo debe contener como mínimo:

- Identificador.
- Nombre.
- Tipo de activo.
- Ubicación.
- Estado.
- Fecha de registro.

Ejemplos: cámara de tráfico, panel de mensaje variable, semáforo, servidor, equipo de comunicaciones, sensor o estación meteorológica.

### 3.2 Gestión de órdenes de trabajo

La aplicación debe permitir crear, listar y consultar órdenes, asociarlas a un activo y cambiar su estado.

Cada orden debe contener como mínimo:

- Identificador.
- Activo asociado.
- Título.
- Descripción.
- Prioridad: Baja, Media o Alta.
- Estado: Pendiente, En progreso o Finalizada.
- Fecha de creación.

## 4. Reglas de negocio obligatorias

1. Una orden debe estar asociada a un activo existente.
2. No se debe crear un activo sin nombre, tipo y ubicación.
3. No se debe crear una orden sin título, descripción, prioridad y activo.
4. Toda orden inicia en `Pendiente`.
5. El flujo permitido es `Pendiente -> En progreso -> Finalizada`.
6. Una orden finalizada no puede regresar a un estado anterior.
7. Los datos deben validarse y los errores deben mostrarse mediante mensajes comprensibles.
8. Un activo con órdenes asociadas puede desactivarse, pero no debe eliminarse físicamente.

## 5. Requerimientos técnicos

El candidato puede utilizar las tecnologías con las que tenga mayor familiaridad.

### Frontend

- HTML, CSS y JavaScript.
- React.
- Angular.
- Vue.
- Otra tecnología equivalente.

### Backend

- Java con Spring Boot.
- C# con ASP.NET Core.
- JavaScript o TypeScript con Node.js.
- Python con Flask, FastAPI o Django.
- PHP.
- Otra tecnología equivalente.

### Persistencia

- PostgreSQL.
- MySQL.
- SQL Server.
- SQLite.
- MongoDB.
- Archivo JSON.
- Persistencia en memoria, documentando su limitación.

No es obligatorio utilizar una tecnología específica. También se acepta una aplicación monolítica con separación clara entre interfaz, lógica de negocio y acceso a datos.

## 6. Interfaz mínima

### Activos

- Lista de activos.
- Formulario de creación.
- Edición.
- Detalle.
- Desactivación.

### Órdenes

- Lista de órdenes.
- Formulario de creación.
- Selección del activo asociado.
- Detalle.
- Actualización de estado.

El diseño gráfico no es el criterio principal, pero la interfaz debe ser comprensible y funcional.

## 7. Manejo de errores

Se deben controlar al menos:

- Campos obligatorios vacíos.
- Activo inexistente.
- Orden inexistente.
- Cambio de estado no permitido.
- Errores al guardar o consultar información.

## 8. Uso de Git

La solución debe entregarse en un repositorio Git. Se espera:

- Varios commits durante el desarrollo.
- Mensajes comprensibles.
- Archivo `.gitignore` apropiado.
- No versionar dependencias, credenciales ni archivos generados innecesarios.

No se requiere un flujo avanzado de ramas.

## 9. Pruebas

Debe incluirse como mínimo una prueba automatizada sobre una funcionalidad importante, por ejemplo:

- Crear un activo correctamente.
- Rechazar un activo sin nombre.
- Crear una orden asociada a un activo.
- Rechazar una orden sin activo.
- Impedir que una orden finalizada regrese a `En progreso`.

Si no se logra implementar una prueba automatizada, se debe documentar qué se probaría, escenario, resultado esperado y casos de error.

## 10. Documentación de la solución

La entrega debe documentar:

- Tecnologías utilizadas.
- Instrucciones de instalación y ejecución.
- Estructura del proyecto.
- Decisiones técnicas principales.
- Limitaciones conocidas.
- Mejoras futuras.

## 11. Entregables

- Código fuente.
- `README.md` actualizado.
- `.gitignore`.
- Instrucciones de instalación y ejecución.
- Mecanismo de persistencia o script de base de datos.
- Pruebas o evidencia de los escenarios de prueba.
- Respuestas a `REFINEMENT.md`.
- Historial de commits.

## 12. Funcionalidades adicionales

Son opcionales y pueden generar puntos adicionales:

- Dockerfile.
- Docker Compose.
- Autenticación.
- Dashboard.
- Filtros y búsquedas.
- Paginación.
- Pruebas adicionales.
- Swagger/OpenAPI.
- CI/CD.
- Manejo de usuarios o responsables.
- Historial de cambios.
- Diseño responsive.
- Despliegue público.

No deben priorizarse antes del alcance obligatorio.

## 13. Uso de inteligencia artificial

Se permite utilizar herramientas de IA como apoyo para consultar conceptos, entender errores, revisar documentación o mejorar redacción. El candidato debe comprender y poder explicar el código entregado.

## 14. Sustentación

El candidato tendrá aproximadamente **15 a 20 minutos** para presentar:

1. Problema entendido.
2. Solución construida.
3. Estructura utilizada.
4. Demostración funcional.
5. Principales dificultades.
6. Mejoras futuras.

Posteriormente se realizará una conversación técnica.

## 15. Recomendaciones finales

- Lee toda la prueba antes de comenzar.
- Revisa `BACKLOG.md`.
- Responde `REFINEMENT.md`.
- Prioriza las funcionalidades obligatorias.
- Realiza commits progresivos.
- Valida los datos.
- Documenta decisiones y pendientes.
- No incluyas contraseñas, tokens o información privada.
- Construye una solución que puedas explicar.

¡Éxitos en la prueba!
