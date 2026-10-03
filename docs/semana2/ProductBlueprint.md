# Product Blueprint — Horizonte Vivo

## Priorización de historias

> Historias elegidas entre las que propuso el equipo y criterio con que se priorizaron. Son las que pasan al backlog.

El equipo reunió **35 historias de usuario** (7 por integrante) y las priorizó con tres criterios:

1. **Impacto directo en la crisis humanitaria del terremoto del 10 de agosto de 2026** (335 muertos, 486,917 damnificados, déficit humanitario del 52%).
2. **Resolución de la causa raíz identificada en el Problem Brief** (falta de trazabilidad y de registro compartido).
3. **Viabilidad técnica dentro del alcance del MVP** con Stellar.

Las **10 historias priorizadas** que pasan al backlog son:

| # | Historia priorizada | Rol | Por qué entra al MVP |
|---|---|---|---|
| 1 | Registrar la salida de un lote hacia un grupo beneficiario | Centro de acopio | Punto crítico de trazabilidad (Gustavo Arcila) |
| 2 | Registrarme como beneficiario con mis necesidades básicas | Damnificado / vulnerable | Sin registro previo, el sistema es ciego (Ricardo Escobar) |
| 3 | Registrar la producción de compost a partir de residuos orgánicos | Huerta comunitaria | Cierra el ciclo ambiental demostrable (Sebastián) |
| 4 | Recibir un certificado digital verificable de mi donación | Empresa donante | Incentivo económico clave (Robinson Quintero) |
| 5 | Permitir que un tercero de confianza me registre en la red | Persona mayor sin pensión | Resuelve la invisibilidad inicial (Santiago Franco) |
| 6 | Registrar la entrada de cada lote de donación recibida | Centro de acopio | Constancia pública de lo recibido (Gustavo Arcila) |
| 7 | Consultar el estado de mi donación en tiempo real | Donante | Cierra el ciclo de confianza (Robinson Quintero) |
| 8 | Ver el historial de atenciones de una persona vulnerable | Trabajador social | Evita duplicación y da continuidad (Santiago Franco) |
| 9 | Registrar kilogramos de material reciclable recolectado | Colegio participante | Evidencia educativa y ambiental (Sebastián) |
| 10 | Consultar impacto ambiental agregado por comuna | Ciudadano | Transparencia y participación (Sebastián) |

El resto de historias quedan como **backlog futuro** (post-MVP).

---

## Propuesta de valor

> Qué resultado obtiene el usuario y por qué elegiría esta solución. En qué se diferencia de cómo resuelve hoy. Conecta con el usuario del Problem Brief.

**Horizonte Vivo convierte la buena voluntad dispersa en un sistema verificable de trazabilidad de recursos y atenciones.**

Para el **damnificado del terremoto** y la **persona vulnerable**, Horizonte Vivo ofrece algo que hoy no existe: un registro verificable que garantiza que será identificado y atendido, incluso si no tiene dirección fija, teléfono o documentos. Hoy su única opción es esperar que alguien se acuerde de él; con Horizonte Vivo, existe un historial público de que fue registrado y de qué ayuda le corresponde.

Para la **empresa donante**, Horizonte Vivo reemplaza la incertidumbre por un certificado digital verificable de que su donación llegó a destino. Hoy dona y recibe una foto; con Horizonte Vivo, ve el recorrido completo y accede a beneficios tributarios cuando la ley lo permita.

Para la **fundación, iglesia o centro de acopio**, Horizonte Vivo elimina la dependencia de la palabra personal. Hoy su transparencia depende de que les crean; con Horizonte Vivo, cada entrada y salida queda registrada de forma inalterable y auditable sin exponer datos personales.

**Diferencial clave:** no es una base de datos más. Es un registro compartido donde ninguna parte puede modificar unilateralmente lo que ocurrió, lo que hace posible confiar entre actores que hoy no confían entre sí.

---

## Flujo de usuario

> Recorrido de la persona por la solución de principio a fin, roles y puntos de interacción. Diagrama o secuencia numerada.

**Flujo principal — Donación empresarial en emergencia:**

1. **Empresa donante** ingresa a la plataforma y registra un lote de donación (categoría, cantidad, fecha, ubicación). → *Interacción con Stellar: se firma una transacción de registro.*
2. **Horizonte Vivo** notifica al centro de acopio más cercano y asigna un vehículo de recolección.
3. **Conductor del vehículo** confirma la recogida en la app. → *Stellar: segunda transacción, vincula lote con vehículo.*
4. **Centro de acopio** registra la entrada del lote, clasifica y actualiza el inventario. → *Stellar: tercera transacción, entrada verificable.*
5. **Trabajador social / líder comunitario** consulta el inventario y asigna el lote a un grupo de beneficiarios registrados previamente.
6. **Centro de acopio** registra la salida del lote hacia ese grupo. → *Stellar: cuarta transacción, cierra la trazabilidad.*
7. **Beneficiario** recibe el lote; su historial se actualiza automáticamente.
8. **Empresa donante** recibe notificación y certificado digital verificable. → *Stellar: consulta pública del historial del lote.*

**Flujo paralelo — Ciclo ambiental:**

1. **Colegio** recolecta material reciclable y lo registra. → *Stellar: transacción de origen.*
2. **Centro de acopio** clasifica y envía a **empresa transformadora**.
3. **Residuos orgánicos** van a **huerta comunitaria**, que registra producción de compost. → *Stellar: transacción de transformación.*
4. **Huerta** vincula el compost con alimentos producidos. → *Stellar: transacción de ciclo cerrado.*

**Puntos de interacción:** app móvil (donante, conductor, trabajador social), panel web (centro de acopio, fundación, auditor), consulta pública (donante, veedor, ciudadano).

---

## Alcance del MVP

> Funcionalidad central separada de la deseable que queda fuera. Justificación de por qué el recorte sigue entregando valor.

**Funcionalidad central del MVP (10 historias priorizadas):**

- Registro de donaciones por parte de empresas (entrada al sistema).
- Registro de entradas y salidas en centros de acopio (trazabilidad core).
- Registro de beneficiarios vulnerables (incluyendo registro por tercero).
- Registro de atenciones a beneficiarios (historial verificable).
- Certificado digital verificable de donación (incentivo económico).
- Consulta pública del estado de una donación (transparencia).
- Registro de recolección de reciclaje en colegios.
- Registro de producción de compost en huertas.
- Consulta agregada de impacto ambiental por comuna.
- Consulta de historial de atenciones por trabajador social.

**Queda fuera del MVP (deseable para fases posteriores):**

- Manufactura textil y comercialización de indumentaria empresarial.
- Comercialización de compost empacado a gran escala.
- Integración con sistemas gubernamentales (UNGRD, Medellín Te Quiere).
- Módulo de protección animal.
- Gamificación y recompensas para jóvenes participantes.
- Trazabilidad de biopolímeros.
- App nativa para iOS/Android (el MVP será web responsive + PWA).

**Justificación del recorte:** el MVP se enfoca en **cerrar el ciclo de trazabilidad de donaciones y atenciones**, que es la causa raíz del problema. Esto ya entrega valor tangible: una empresa puede donar con confianza, un damnificado puede ser registrado y atendido, y un centro de acopio puede demostrar transparencia. Las funcionalidades dejadas fuera amplían el impacto pero no son necesarias para demostrar que la hipótesis del Problem Brief funciona.

---

## Lean Canvas

> Lienzo de una página con el modelo del producto.

![Lean Canvas Horizonte Vivo](docs/semana2/lean-canvas.png)

**Enlace alternativo:** [Lean Canvas en Miro](https://miro.com/app/board/horizonte-vivo-lean-canvas)

| Bloque | Contenido |
|---|---|
| **Problema** | Donaciones sin trazabilidad; personas vulnerables invisibles; centros de acopio sin evidencia; empresas sin incentivo; residuos aprovechables perdidos. |
| **Segmentos de usuarios** | Empresas donantes; fundaciones e iglesias; centros de acopio; damnificados y personas vulnerables; colegios y huertas; auditores y veedores. |
| **Propuesta de valor única** | Trazabilidad verificable e inalterable de cada donación, atención y material, desde el origen hasta el destino final. |
| **Solución** | Plataforma web + PWA; registro en Stellar; certificados digitales; consulta pública; paneles de impacto. |
| **Canales** | Alianzas con iglesias, fundaciones, colegios, universidades, empresas y gobiernos locales; redes comunitarias; GitHub y Apex para el piloto académico. |
| **Métricas clave** | N° de donaciones registradas; % de trazabilidad completa (origen→destino); N° de beneficiarios registrados; kg de material aprovechado; N° de certificados emitidos; tiempo promedio de ciclo de donación. |
| **Ventaja diferencial** | Registro compartido e inalterable entre actores que no confían entre sí; enfoque simultáneo en emergencia y operación diaria; integración con economía circular. |
| **Estructura de costos** | Desarrollo y mantenimiento de plataforma; costos de transacción en Stellar (mínimos); logística de recolección; capacitación; operación de centros de acopio. |
| **Fuentes de ingresos** | Certificaciones digitales para empresas; comercialización de compost y materiales reciclados; contratos de manufactura textil (post-MVP); donaciones económicas empresariales; posibles subsidios públicos y cooperación internacional. |

---

## Backlog priorizado (Kanban)

> Enlace al tablero en GitHub Projects, construido con las historias priorizadas, en columnas y con criterios de aceptación por tarjeta.

**🔗 Tablero Kanban:** [Horizonte Vivo — Backlog MVP](https://github.com/users/horizonte-vivo/projects/1)

**Columnas del tablero:**
- 📋 **Backlog** (todas las historias priorizadas)
- 🎯 **Ready** (listas para desarrollar, con criterios de aceptación claros)
- 🚧 **In Progress** (en desarrollo)
- 👀 **Review** (en revisión)
- ✅ **Done** (completadas)

**Ejemplo de criterios de aceptación por tarjeta:**

**Tarjeta #1: Registrar salida de lote hacia grupo beneficiario**
- **Como** administrador de centro de acopio
- **Quiero** registrar la salida de un lote hacia un grupo beneficiario
- **Para** demostrar objetivamente que lo repartí
- **Criterios de aceptación:**
  - [ ] El formulario exige lote, grupo beneficiario y fecha.
  - [ ] La transacción queda firmada en Stellar.
  - [ ] El registro no puede editarse ni borrarse después.
  - [ ] El donante recibe notificación automática.
  - [ ] El veedor puede consultar el movimiento sin ver datos personales.

**Tarjeta #2: Registrarme como beneficiario con mis necesidades básicas**
- **Como** damnificado del terremoto
- **Quiero** registrarme como beneficiario con mis necesidades básicas
- **Para** que las ayudas lleguen a mí de forma priorizada
- **Criterios de aceptación:**
  - [ ] El formulario permite categorizar necesidades (alimento, vestuario, refugio, salud).
  - [ ] El registro puede hacerse por un tercero de confianza.
  - [ ] Los datos personales quedan protegidos y solo visibles para trabajadores sociales autorizados.
  - [ ] El beneficiario recibe un identificador digital verificable.

*(Y así sucesivamente para las 10 historias priorizadas.)*

---

## Arquitectura inicial

> Cómo se conectan las partes (interfaz, lógica, Stellar) y en qué punto entra la red. Diagrama simple.
