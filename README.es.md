# OpenCode Toolkit

[English](README.en.md) | **Español**

Guía práctica de comandos, gestión de contexto y productividad para el desarrollo asistido por inteligencia artificial.

## Introducción

OpenCode Toolkit es una guía de referencia para comprender comandos, organizar sesiones de trabajo y mejorar los flujos de desarrollo con agentes de programación basados en IA.

El objetivo es explicar para qué sirve cada comando, cuáles son sus limitaciones y qué buenas prácticas conviene aplicar para proteger el trabajo realizado.

## Comandos

### 1. `/init`

Prepara el contexto inicial de un proyecto y, en los entornos compatibles, ayuda a generar instrucciones para que el agente comprenda su estructura y sus convenciones.

```text
/init
```

**Limitaciones**
- No garantiza que el agente comprenda todos los archivos, dependencias o decisiones arquitectónicas.
- Las instrucciones generadas pueden ser incompletas o quedar desactualizadas.
- No sustituye la revisión del código ni la ejecución de pruebas.
- No garantiza que el contexto se conserve automáticamente entre sesiones.

**Buena práctica:** revisa las instrucciones generadas y mantenlas actualizadas conforme evolucione el proyecto.

### 2. `/models`

Permite consultar o seleccionar modelos cuando el entorno implementa este comando.

```text
/models
```

**Limitaciones**
- Los modelos disponibles dependen del proveedor, la configuración y las capacidades del entorno.
- Los modelos pueden diferir en calidad, velocidad, contexto y coste.
- Un modelo más económico no siempre reduce el coste total si requiere más intentos.
- Cambiar de modelo no garantiza conservar todo el contexto anterior.

**Buena práctica:** utiliza modelos ligeros para tareas sencillas y modelos más capaces para problemas complejos, después de comprobar sus costes y limitaciones.

### 3. `/sessions`

Facilita el acceso a sesiones anteriores cuando la herramienta ofrece funciones de historial y recuperación.

```text
/sessions
```

**Limitaciones**
- Solo pueden recuperarse las sesiones que se hayan conservado y estén disponibles.
- Abrir una sesión anterior no garantiza restaurar procesos, variables, archivos temporales o estados externos.
- El historial disponible depende de la configuración y de la herramienta.
- Una sesión recuperada puede no contener todo el contexto necesario para continuar.

**Buena práctica:** registra el progreso, las decisiones y las tareas pendientes en archivos persistentes del proyecto.

### 4. `/compact`

Reduce o resume el contexto de una conversación cuando el entorno admite esta funcionalidad.

```text
/compact
```

**Limitaciones**
- El resumen puede omitir detalles, ejemplos, decisiones secundarias o fragmentos de código.
- No garantiza conservar literalmente toda la conversación.
- No aumenta necesariamente el límite máximo de contexto del modelo.
- No sustituye las copias de seguridad ni el almacenamiento de información importante.

**Buena práctica:** conserva los requisitos críticos, los comandos relevantes y el estado actual del proyecto en archivos como `README.md`, `AGENTS.md` o documentos de seguimiento.

### 5. `/undo`

Solicita revertir una acción o un cambio anterior cuando la herramienta proporciona esta funcionalidad.

```text
/undo
```

**Limitaciones**
- El alcance de la reversión depende de la implementación.
- No garantiza deshacer todas las modificaciones realizadas durante una sesión.
- Los cambios en sistemas externos o acciones irreversibles pueden no recuperarse.
- No debe considerarse un sustituto del control de versiones.

**Buena práctica:** utiliza Git para registrar los cambios y poder revisar o recuperar versiones anteriores del proyecto.

## Recomendaciones generales

1. Inicializa el contexto del proyecto antes de empezar a trabajar.
2. Selecciona el modelo según la complejidad de la tarea y el coste esperado.
3. Guarda el progreso en archivos persistentes para facilitar la continuidad entre sesiones.
4. Resume las conversaciones largas solo después de identificar la información crítica.
5. Utiliza Git y revisa los cambios antes de aplicar operaciones destructivas.

## Compatibilidad

Los comandos descritos en esta guía no deben considerarse comandos universales. Su disponibilidad y comportamiento dependen de la versión de OpenCode, las extensiones instaladas, la configuración y las herramientas externas utilizadas.

Comprueba la documentación oficial de tu entorno antes de asumir que un comando está disponible o funciona de una forma específica.

---

[Volver a la portada](README.md)
