# Horizonte Vivo --- Functional Proof

## Descripción del proyecto

**Horizonte Vivo** es un proyecto de innovación social, ambiental y
educativa que busca conectar personas, instituciones educativas,
comunidades, fundaciones, empresas y voluntarios para organizar
iniciativas territoriales y dar seguimiento a sus resultados. La
propuesta parte de una problemática: existen necesidades sociales y
ambientales, recursos aprovechables y personas dispuestas a participar,
pero estas capacidades no siempre están coordinadas ni cuentan con una
forma común de registrar sus actividades e impacto.

La plataforma busca facilitar la publicación y consulta de iniciativas,
la participación de distintos actores y la visualización de información
sobre las acciones realizadas. Entre sus líneas de trabajo se encuentran
la educación ambiental, la separación y aprovechamiento de residuos, las
huertas, el voluntariado, la participación comunitaria y el apoyo a
proyectos sociales. Dos iniciativas representativas son **La Liga
Ambiental**, enfocada en promover la participación de instituciones
educativas en actividades de separación y aprovechamiento de residuos, y
**Sembrando Futuro: Familias, Escuela y Comunidad**, orientada a
impulsar actividades educativas y ambientales con participación de
jóvenes, familias y comunidades.

El propósito del MVP es mostrar de forma clara cómo una persona puede
conocer Horizonte Vivo, explorar iniciativas y comprender cómo
participar en ellas. La interfaz debe representar el flujo principal
definido en el Product Blueprint y servir como prueba funcional visual
del producto. Las funcionalidades que todavía no estén conectadas a una
base de datos, autenticación o servicios externos deben presentarse como
demostraciones de interfaz, sin afirmar que ya operan en producción.

## Objetivo del Functional Proof

Construir una versión navegable del frontend que permita comprender la
propuesta de Horizonte Vivo y recorrer las pantallas principales del
MVP. El frontend debe priorizar una navegación sencilla, una
presentación clara de las iniciativas y una experiencia consistente en
la que el usuario pueda identificar el propósito del proyecto y las
formas de participación contempladas.

## Flujo principal propuesto para el frontend

1.  **Inicio:** presenta el propósito de Horizonte Vivo, sus líneas de
    acción y accesos a las iniciativas.
2.  **Explorar iniciativas:** permite consultar proyectos o actividades
    sociales, ambientales y educativas.
3.  **Detalle de una iniciativa:** muestra su descripción, objetivo,
    ubicación o comunidad destinataria cuando esté definida, actividades
    y resultados esperados.
4.  **Participación:** explica cómo una persona o institución puede
    expresar interés o participar. Si el envío aún no está conectado a
    un backend, debe mostrarse como una interacción demostrativa.
5.  **Impacto:** presenta indicadores que la plataforma busca registrar,
    como kilogramos de residuos recuperados, árboles sembrados, personas
    participantes, instituciones involucradas y horas de voluntariado.
    Los datos de ejemplo deben identificarse claramente como
    demostrativos y no como resultados reales.

> **Importante:** ajustar este flujo a las pantallas y al recorrido que
> efectivamente se hayan definido en el Product Blueprint. No documentar
> como implementadas funciones que todavía no existen en el frontend.

## Front construido

Completar esta sección con información verificada del repositorio:

-   **Tecnologías utilizadas:** \[indicar framework, lenguaje y
    herramientas\].
-   **Pantallas implementadas:** \[enumerar las pantallas que realmente
    existen\].
-   **Navegación:** \[explicar cómo se pasa de una pantalla a otra\].
-   **Interacciones funcionales:** \[botones, filtros, formularios o
    acciones que sí funcionan\].
-   **Capturas o demo:** \[añadir capturas o URL pública, si existe\].
-   **Relación con el MVP:** explicar qué parte del flujo del Product
    Blueprint demuestra cada pantalla.

## Decisión técnica: uso de Stellar y contratos

**Esta decisión debe confirmarse con el Product Blueprint del equipo
antes de entregar.** La documentación disponible sobre Horizonte Vivo no
especifica todavía qué dato o proceso se registrará en Stellar, por lo
que no sería correcto afirmar una decisión técnica definitiva sin
revisar ese diseño.

Registrar aquí una de las dos opciones requeridas por la actividad:

### Opción A --- Contrato propio

Si el equipo elige esta opción, explicar qué acción concreta del
producto necesita ejecutarse o registrarse en la red Stellar, qué datos
mínimos manejaría el contrato y por qué la lógica requiere un contrato
propio. En esta semana solo se documenta la decisión; no es necesario
escribir ni desplegar el contrato.

### Opción B --- Herramienta existente del ecosistema Stellar

Si el equipo elige esta opción, nombrar la herramienta o servicio
específico, describir para qué se utilizará y explicar por qué satisface
la necesidad del MVP mejor que desarrollar un contrato propio.

**Decisión final del equipo:** \[Opción A u Opción B\].

**Justificación basada en el Product Blueprint:** \[describir el caso de
uso concreto de Stellar, la información o transacción involucrada y la
razón de la elección\].

**Nota de alcance:** durante esta entrega se trabaja únicamente con la
testnet, según las instrucciones del ejercicio. No afirmar que existen
contratos desplegados si todavía no se han implementado.

## Participación del equipo

  -----------------------------------------------------------------------
  Integrante              Usuario de GitHub       Aporte en este
                                                  entregable
  ----------------------- ----------------------- -----------------------
  \[Nombre\]              [@usuario]              \[Pantalla, componente
                                                  o documentación
                                                  desarrollada\]

  \[Nombre\]              [@usuario]              \[Pantalla, componente
                                                  o documentación
                                                  desarrollada\]

  \[Nombre\]              [@usuario]              \[Pantalla, componente
                                                  o documentación
                                                  desarrollada\]
  -----------------------------------------------------------------------

Cada integrante debe realizar al menos un commit propio durante la
semana. Completar esta tabla según las contribuciones reales y
comprobarlas en el historial del repositorio.

## Bloqueos y siguiente paso

**Bloqueos actuales:** \[indicar problemas reales: integración,
navegación, contenido, configuración o decisión sobre Stellar\].

**Siguiente paso:** completar y probar el flujo principal del frontend,
verificar que el proyecto pueda ejecutarse siguiendo el README,
confirmar la decisión técnica con el Product Blueprint y preparar la
siguiente etapa de implementación.

## Verificación antes de entregar

-   [ ] El frontend se ejecuta y permite recorrer el flujo principal.
-   [ ] Las pantallas descritas corresponden a lo implementado.
-   [ ] Las capturas o el enlace de demostración están incluidos, si
    corresponde.
-   [ ] Cada integrante tiene al menos un commit propio.
-   [ ] La decisión de contratos o herramienta de Stellar está elegida y
    justificada.
-   [ ] El README contiene únicamente requisitos, instalación y comandos
    para ejecutar el proyecto.
-   [ ] El repositorio se carga en Apex según las instrucciones del
    curso.
