# Sales Knowledge AI Agent

Agente de inteligencia artificial diseñado para NexaShip con el objetivo de facilitar el acceso al conocimiento interno empresarial mediante preguntas en lenguaje natural y respuestas basadas en evidencia documental.

## Descripción del proyecto

Sales Knowledge AI Agent es una solución orientada a mejorar la forma en que los equipos de NexaShip consultan y utilizan el conocimiento interno necesario para atender preguntas comerciales y tomar decisiones durante la gestión de oportunidades.

En un entorno empresarial con diferentes áreas de especialización, la información puede encontrarse distribuida entre políticas, manuales, procedimientos y personas con distintas skills.

Como consecuencia, una consulta puede depender de la disponibilidad de líderes o especialistas específicos, generando tiempos de espera y dificultando el acceso oportuno a la información.

El proyecto propone centralizar el acceso a este conocimiento mediante un agente de IA capaz de interpretar preguntas en lenguaje natural, recuperar información relevante desde la documentación interna disponible y generar respuestas sustentadas en evidencia.

---

## Contexto de NexaShip

NexaShip es una empresa de tecnología logística que ofrece una plataforma digital para centralizar y optimizar la gestión de envíos de negocios, tiendas en línea y empresas con operaciones de alto volumen.

Su solución facilita la gestión de operaciones logísticas y la conexión con diferentes herramientas tecnológicas utilizadas por sus clientes.

A medida que la organización crece, también aumenta el conocimiento relacionado con:

- políticas internas;
- condiciones comerciales;
- integraciones tecnológicas;
- procesos operativos;
- gestión de incidencias;
- protección de información;
- criterios de escalamiento;
- situaciones especiales de clientes.

Parte de este conocimiento puede requerir la intervención de personas con diferentes skills y áreas de especialización.

---

## Problema identificado

Los equipos comerciales de NexaShip pueden necesitar resolver consultas relacionadas con políticas, condiciones comerciales, integraciones, operaciones o situaciones especiales antes de responder a un prospecto o cliente.

Sin embargo, cuando el conocimiento se encuentra distribuido entre diferentes fuentes o depende de especialistas específicos, pueden presentarse situaciones como:

- tiempos prolongados de espera;
- consultas enviadas al especialista incorrecto;
- dependencia de la disponibilidad de líderes;
- respuestas basadas en conocimiento informal;
- duplicación de preguntas entre equipos;
- pérdida de contexto durante un escalamiento;
- retrasos en oportunidades comerciales;
- consultas que pueden quedar sin respuesta.

Por ejemplo, una persona del equipo comercial podría necesitar resolver preguntas como:

- ¿Puedo ofrecer una condición comercial especial?
- ¿Qué nivel de aprobación requiere un descuento?
- ¿Puedo confirmar una integración que no aparece documentada?
- ¿Qué debo hacer si solo encuentro información parcial?
- ¿A qué especialidad corresponde una consulta?
- ¿Cuándo una situación requiere revisión multidisciplinaria?

Resolver estas preguntas manualmente puede requerir revisar documentación o esperar la disponibilidad de una persona especialista.

---

## Solución propuesta

Sales Knowledge AI Agent busca proporcionar un punto de consulta inteligente para el conocimiento interno de NexaShip.

La solución permitirá que una persona colaboradora formule preguntas en lenguaje natural y reciba respuestas sustentadas en la documentación interna disponible.

El comportamiento esperado del agente es:

1. recibir una pregunta en lenguaje natural;
2. interpretar la necesidad de la persona usuaria;
3. consultar la fuente documental disponible;
4. recuperar la información relevante;
5. evaluar si existe evidencia suficiente;
6. generar una respuesta sustentada en el contenido recuperado;
7. evitar completar información faltante mediante suposiciones;
8. reconocer cuándo la documentación no permite responder con seguridad;
9. orientar el escalamiento según la especialidad requerida cuando corresponda.

El objetivo no es únicamente responder preguntas, sino reducir la dependencia de búsquedas manuales y evitar respuestas sin respaldo documental.

---

## Objetivos del proyecto

### Objetivo general

Desarrollar un agente de inteligencia artificial que facilite a los equipos de NexaShip la consulta de conocimiento interno mediante lenguaje natural.

### Objetivos específicos

- reducir el tiempo dedicado a buscar información interna;
- facilitar el acceso a políticas y lineamientos vigentes;
- generar respuestas basadas en evidencia documental;
- reducir respuestas construidas a partir de suposiciones;
- identificar situaciones con información insuficiente;
- apoyar la clasificación de consultas según la skill requerida;
- orientar posibles rutas de escalamiento;
- construir una solución extensible hacia múltiples fuentes documentales.

---

## Alcance actual del MVP

La primera versión del proyecto utiliza una única fuente documental:

`Politicas_Internas_NexaShip.pdf`

El documento consolida lineamientos internos relacionados con:

- gestión comercial;
- confirmación de capacidades y servicios;
- descuentos y negociaciones;
- protección y manejo de datos;
- escalamiento interno;
- clasificación de consultas por skill;
- niveles de escalamiento;
- casos especiales;
- prohibiciones y responsabilidades.

El objetivo inicial es validar el funcionamiento del agente utilizando una única fuente documental antes de ampliar progresivamente la solución.

---

## Fuente documental inicial

La fuente de conocimiento del MVP se encuentra en:

`data/documents/Politicas_Internas_NexaShip.pdf`

Este documento constituye la primera fuente documental utilizada para construir y evaluar el comportamiento del agente.

A partir de su contenido se podrán probar consultas relacionadas con políticas comerciales, niveles de autorización, manejo de información, clasificación por skills y criterios de escalamiento.

---

## Arquitectura conceptual del MVP

```text
Persona colaboradora de NexaShip
              |
              v
Pregunta en lenguaje natural
              |
              v
Sales Knowledge AI Agent
              |
              v
Procesamiento de la consulta
              |
              v
Búsqueda de información relevante
              |
              v
Politicas_Internas_NexaShip.pdf
              |
              v
Evaluación de evidencia
              |
       +------+------+
       |             |
       v             v
  Evidencia      Evidencia
  suficiente     insuficiente
       |             |
       v             v
   Respuesta      No inventar
   basada en      información
   documento          |
                      v
                 Orientar posible
                  escalamiento
```

La implementación técnica será documentada y actualizada progresivamente conforme avance el desarrollo.

---

## Principios de comportamiento del agente

Sales Knowledge AI Agent será desarrollado bajo los siguientes principios:

### Respuestas basadas en evidencia

El agente deberá utilizar la información disponible en las fuentes documentales autorizadas.

### No inventar información

Cuando no exista evidencia suficiente, el agente deberá evitar completar la respuesta mediante suposiciones.

### Reconocer información parcial

Si la documentación permite responder solo una parte de la consulta, el agente deberá diferenciar entre información confirmada e información pendiente de validación.

### Orientar el escalamiento

Cuando una consulta requiera conocimiento especializado, el agente podrá orientar la clasificación según la skill correspondiente.

### Mantener trazabilidad

La evolución del proyecto buscará permitir que las respuestas puedan relacionarse con las fuentes utilizadas.

---

## Evolución prevista

Una vez validado el MVP con una única fuente documental, la solución podrá ampliarse progresivamente.

Entre las mejoras previstas se encuentran:

- incorporación de manuales operativos;
- incorporación de procedimientos internos;
- consulta de múltiples documentos;
- procesamiento de archivos CSV;
- catálogo estructurado de servicios;
- matriz de skills;
- matriz de escalamiento;
- recuperación de información desde diferentes fuentes;
- trazabilidad de evidencia;
- interfaz de consulta;
- despliegue de la aplicación en la nube.

La evolución propuesta permitirá pasar de un agente basado en un único documento a una solución de consulta de conocimiento empresarial multidocumental.

---

## Estructura actual del repositorio

```text
sales-knowledge-ai-agent/
|
├── data/
│   └── documents/
│       └── Politicas_Internas_NexaShip.pdf
|
├── .gitignore
├── LICENSE
└── README.md
```

La estructura será ampliada progresivamente conforme avance la implementación.

---

## Estado del proyecto

**En desarrollo — Fase MVP**

### Estado actual

- definición del problema empresarial;
- diseño de la solución propuesta;
- definición del alcance inicial;
- creación de la primera fuente documental;
- preparación de la base del proyecto.

### Próxima etapa

- implementación del procesamiento inicial del documento PDF.

---

## Escalabilidad del proyecto

La arquitectura del proyecto se plantea de forma progresiva.

### Fase 1 — MVP documental

Consulta de una única fuente PDF.

### Fase 2 — Conocimiento multidocumental

Incorporación de políticas, manuales y procedimientos.

### Fase 3 — Fuentes estructuradas

Integración de archivos CSV relacionados con servicios, skills y escalamiento.

### Fase 4 — Experiencia de consulta

Incorporación de una interfaz para facilitar la interacción con el agente.

### Fase 5 — Despliegue

Publicación de la solución en infraestructura cloud.

---

## Nota sobre el escenario

NexaShip y la documentación incluida en este repositorio corresponden a un escenario empresarial simulado con fines educativos y demostrativos.

Las políticas, procesos, roles y reglas utilizadas en el proyecto fueron diseñadas específicamente para el desarrollo del challenge y no representan información interna de una empresa real.

---

## Licencia

Este proyecto se distribuye bajo la licencia MIT.
