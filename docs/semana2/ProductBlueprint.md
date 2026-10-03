# Product Blueprint — Horizonte Vivo

**Repositorio:** `https://github.com/Andruw5/[nombre-del-repo]`
**Tablero Kanban:** `https://github.com/users/Andruw5/projects/[número]`
**Semana:** 2 — Entregable 2
**Fecha límite:** Domingo 4 de octubre, 6:00 p.m. hora Colombia

---

## Priorización de historias

> Historias elegidas entre las que propuso el equipo y criterio con que se priorizaron. Son las que pasan al backlog.

El equipo reunió **35 historias de usuario** (7 por integrante) y priorizó **12** para el MVP, usando tres criterios:

1. **Impacto directo en el problema raíz:** historias que sin ellas el sistema no funciona (registro de personas vulnerables, registro de salida de lotes, anclaje inalterable).
2. **Habilitadoras de otras historias:** historias que desbloquean el resto de la cadena (registro previo, firma digital, identificador único).
3. **Valor verificable para el usuario final:** historias que producen evidencia concreta para donantes, veedores o beneficiarios.

**Historias priorizadas para el MVP:**

| # | Historia | Autor | Criterio | ¿Por qué está en el MVP? |
|---|---|---|---|---|
| H1 | Registrar personas vulnerables con código anónimo | Santiago | Impacto raíz | Sin registro previo, la población vulnerable es invisible |
| H2 | Registrar salida de lote hacia beneficiario | Gustavo | Impacto raíz | Es el punto donde hoy se pierde toda la trazabilidad |
| H3 | Anclar cada donación en registro público e inalterable | Robinson | Habilitadora técnica | Sin inmutabilidad, el resto del sistema no es confiable |
| H4 | Firma digital de la donación al entregarla | Robinson | Habilitadora técnica | Prueba criptográfica de que la donación existió |
| H5 | Identificador único por lote en Stellar | Robinson | Habilitadora técnica | Permite rastrear cualquier lote sin ambigüedad |
| H6 | Registrar entrada de lote en centro de acopio | Sebastián / Gustavo | Cadena logística | Necesario para vincular origen y tránsito |
| H7 | Registrar salida de lote clasificado (reciclable, orgánico, textil) | Sebastián | Cadena ambiental | Sin salida no hay economía circular verificable |
| H8 | Consultar tablero público de donaciones entregadas | Gustavo | Valor verificable | Es lo que el donante realmente quiere ver |
| H9 | Registrar atención a persona vulnerable (alimento, abrigo) | Ricardo | Valor social | Es lo que cierra el ciclo de la red de apoyo |
| H10 | Reporte agregado de donaciones recibidas y entregadas | Gustavo | Transparencia | Necesario para fundaciones y cooperación internacional |
| H11 | Verificar cadena completa sin datos personales | Robinson | Auditoría | Permite veeduría ciudadana sin violar privacidad |
| H12 | Mapa agregado de personas vulnerables atendidas y pendientes | Santiago | Coordinación territorial | Permite distribuir recursos de forma más justa |

**Historias que quedan fuera del MVP (backlog deseable):**
- Mapa interactivo de huertas y puntos de acopio (Sebastián H7).
- Certificación automática de beneficios tributarios (Robinson H4).
- Integración con sistemas de gobierno (UNGRD, INVIMA).
- Módulo de manufactura textil y compost comercial.
- App nativa móvil (el MVP es web responsive).
- Verificación por SMS en zonas sin internet.
- Módulo de protección animal.
- Reporte de impacto ambiental por comuna (Sebastián H6).

---

## Propuesta de valor

> Qué resultado obtiene el usuario y por qué elegiría esta solución. En qué se diferencia de cómo resuelve hoy. Conecta con el usuario del Problem Brief.

Horizonte Vivo le entrega a cada actor una **prueba verificable de que su aporte llegó a destino**, sin depender de la palabra de nadie. Para el **donante empresarial**, significa que puede ver en un tablero público que su donación fue registrada como entregada, y obtener una certificación verificable para posibles beneficios tributarios. Para la **persona mayor sin pensión o en situación de calle**, significa dejar de ser invisible: tendrá un código anónimo y un historial de atenciones que responde por ella incluso cuando nadie cercano puede hacerlo. Para la **fundación o iglesia**, significa poder demostrar transparencia ante donantes y cooperación internacional con reportes generados automáticamente desde el registro anclado. Para el **veedor comunitario o periodista**, significa poder auditar entradas y salidas de un centro de acopio sin acceder a datos personales de beneficiarios.

Hoy todo esto se resuelve con WhatsApp, papel, fotos y buena voluntad, y el costo es que nadie puede verificar nada: ni el donante sabe si su aporte llegó, ni la persona vulnerable tiene cómo probar que fue atendida, ni la fundación tiene cómo defenderse de una sospecha. En el contexto del terremoto del 10 de agosto de 2026 (335 muertos, 486,917 damnificados, déficit humanitario del 52%), esta falta de trazabilidad significó que personas sin dirección verificable quedaran fuera de las listas de ayuda.

La diferencia es que Horizonte Vivo **no reemplaza la logística, le agrega trazabilidad inalterable**. El usuario no cambia su forma de donar ni de atender; cambia la posibilidad de probar lo que hizo. Y a diferencia de una base de datos tradicional, la confianza no depende de un administrador central: depende de la red Stellar, que garantiza que el histórico no puede alterarse.

---

## Flujo de usuario

> Recorrido de la persona por la solución de principio a fin, roles y puntos de interacción. Diagrama o secuencia numerada.

**Flujo principal — Donación de alimentos en emergencia:**

1. **Empresa donante** entra a la app web y registra un lote: categoría (alimento), cantidad, fecha, destino previsto. → El sistema genera un identificador único.
2. **Empresa** firma digitalmente el registro con su cuenta Stellar. → El hash del lote queda anclado en la red.
3. **Centro de acopio** recibe el lote y registra la entrada con el identificador único. → Se vincula al mismo hash en Stellar.
4. **Centro de acopio** clasifica y registra la salida hacia un grupo o familia beneficiaria (o hacia un transformador, en el caso de reciclables).
5. **Líder comunitario** registra la entrega final, vinculando el lote a un código anónimo de beneficiario.
6. **Persona vulnerable** recibe el alimento y, si tiene tarjeta o código, puede verificar que fue registrada (sin necesidad de app).
7. **Donante** consulta el tablero público y ve: lote #X → entregado en fecha Y → destino Z (sin datos personales).
8. **Veedor o periodista** consulta reporte agregado del centro de acopio: entradas vs. salidas, sin datos personales.
9. **Fundación** genera reporte automático para sus donantes o cooperación internacional.

**Roles y puntos de interacción:**

| Rol | Interfaz | Acción principal |
|---|---|---|
| Empresa donante | Web (registro y firma) | Registrar lote y firmar |
| Centro de acopio | Móvil simplificada | Registrar entrada y salida |
| Líder comunitario | Móvil simplificada | Registrar entrega y atención |
| Persona vulnerable | Tarjeta física o SMS | Verificar atención (sin app) |
| Donante / veedor | Tablero público web | Consultar estado y auditoría |
| Fundación | Web (reportes) | Generar reporte agregado |

**Flujo simplificado (diagrama):**
<img width="709" height="300" alt="image" src="https://github.com/user-attachments/assets/06d4869d-216e-48f4-8bb2-c648bbff6aee" />


---

## Alcance del MVP

> Funcionalidad central separada de la deseable que queda fuera. Justificación de por qué el recorte sigue entregando valor.

**Dentro del MVP (funcionalidad central):**

- Registro de personas vulnerables con código anónimo y necesidades básicas.
- Registro de lotes de donación (categoría, cantidad, fecha, origen).
- Firma digital de la donación por parte de la empresa.
- Anclaje en Stellar del hash de cada lote con identificador único.
- Registro de entrada en centro de acopio (vinculado al hash original).
- Registro de salida hacia beneficiario, transformador o huerta.
- Registro de atención a persona vulnerable (alimento, abrigo, visita).
- Tablero público de donaciones entregadas (sin datos personales).
- Reporte agregado por centro de acopio (entradas vs. salidas).
- Verificación de cadena completa por hash público.

**Fuera del MVP (deseable):**

- Mapa interactivo de huertas y puntos de acopio.
- Certificación automática de beneficios tributarios.
- Integración con sistemas de gobierno (UNGRD, INVIMA, Estatuto Tributario).
- Módulo de manufactura textil y compost comercial.
- App nativa móvil (el MVP puede ser web responsive).
- Verificación por SMS en zonas sin internet.
- Módulo de protección animal.
- Reporte de impacto ambiental por comuna.

**Justificación del recorte:**

El MVP se enfoca en **una sola cadena completa** —donación de alimentos en emergencia, desde la empresa hasta la persona vulnerable— porque es la que responde al contexto del terremoto y al problema raíz del Problem Brief. Con esta cadena funcionando de extremo a extremo, el sistema ya entrega valor verificable: el donante ve impacto, el centro de acopio se protege, la persona vulnerable deja de ser invisible y el veedor puede auditar. Lo deseable (mapas, certificaciones, integraciones, otras cadenas) se puede construir encima sin rediseñar el núcleo. El recorte no elimina la esencia del proyecto: **trazabilidad inalterable + protección de datos + foco en emergencias**.

---

## Lean Canvas

> Lienzo de una página con el modelo del producto.

| Bloque | Contenido |
|---|---|
| **Problema** | Donaciones sin trazabilidad; personas vulnerables invisibles; donantes sin evidencia de impacto; fundaciones sin transparencia demostrable; centros de acopio sin protección ante sospechas. |
| **Segmento de usuarios** | Empresas donantes; fundaciones e iglesias; centros de acopio; líderes comunitarios; personas mayores sin pensión, en calle o en abandono; damnificados del terremoto. |
| **Propuesta de valor única** | Prueba verificable de que cada donación llegó a destino, sin exponer datos personales de los beneficiarios. |
| **Solución** | App web/móvil + anclaje en Stellar + tablero público + tarjetas/códigos anónimos para beneficiarios + reportes automáticos. |
| **Canales** | Alianzas con fundaciones, iglesias, colegios, universidades y empresas; redes comunitarias; GitHub como repositorio público; tablero Kanban en GitHub Projects. |
| **Métricas clave** | % de donaciones registradas con trazabilidad completa; tiempo promedio entre donación y entrega verificada; número de personas vulnerables registradas; número de auditorías ciudadanas realizadas; % de reportes generados automáticamente. |
| **Ventaja diferencial** | No reemplaza la logística, la vuelve auditable. Registro inalterable en Stellar + protección de datos con códigos anónimos + foco en emergencias + diseño para población vulnerable. |
| **Estructura de costos** | Desarrollo y mantenimiento de la plataforma; comisiones de red Stellar (muy bajas, ~0.00001 XLM por transacción); capacitación y acompañamiento comunitario; logística de tarjetas/códigos; hosting y base de datos. |
| **Fuentes de ingresos** | Convenios con empresas (RSE + certificación); convenios con fundaciones y cooperación internacional; servicios de reporte para auditoría; venta de compost y productos textiles (fase posterior); donaciones empresariales. |

**Enlace al Lean Canvas (imagen):** `docs/semana2/lean-canvas.png`

---

## Backlog priorizado (Kanban)

> Enlace al tablero en GitHub Projects, construido con las historias priorizadas, en columnas y con criterios de aceptación por tarjeta.

**Enlace al tablero:** `https://github.com/users/Andruw5/projects/[número]`

**Columnas:** Backlog → Ready → In Progress → In Review → Done

**Criterios de aceptación por historia:**

| # | Historia | Criterios de aceptación |
|---|---|---|
| H1 | Registrar personas vulnerables | Crear ficha con código anónimo, necesidades básicas y sector. No mostrar nombre completo en vistas públicas. Validar que el código sea único. |
| H2 | Registrar salida de lote hacia beneficiario | Elegir lote existente, tipo de beneficiario (grupo/familia/persona) y fecha. Generar hash y anclarlo en Stellar. Validar que el lote tenga entrada previa. |
| H3 | Anclar en Stellar | Cada registro debe tener `transaction_hash` verificable en un explorador de Stellar. Si el anclaje falla, no se considera completo el registro. |
| H4 | Firma digital | La empresa debe poder firmar con su clave Stellar. El sistema debe rechazar registros sin firma. La firma debe ser verificable públicamente. |
| H5 | Identificador único por lote | Cada lote debe tener un ID único e inmutable, consultable desde el tablero público. El ID debe vincularse a todos los eventos posteriores. |
| H6 | Registrar entrada en acopio | Vincular el lote al hash original. Registrar fecha, hora y responsable. Validar que el lote no haya sido registrado antes en el mismo centro. |
| H7 | Registrar salida clasificada | Permitir seleccionar tipo (reciclable, orgánico, textil) y destino (transformador, huerta, empresa). Generar hash del evento y anclarlo. |
| H8 | Tablero público | Mostrar estado del lote sin datos personales. Accesible sin login. Verificar hash en Stellar antes de mostrar. |
| H9 | Registrar atención | Permitir registrar tipo de atención (alimento, abrigo, visita, salud), fecha y responsable. No exponer identidad del beneficiario. |
| H10 | Reporte agregado | Generar PDF/CSV con entradas vs. salidas por periodo. Anclar hash del reporte en Stellar. No incluir datos personales. |
| H11 | Verificar cadena sin datos personales | Permitir consultar por hash y mostrar el recorrido completo (origen → tránsito → destino). No mostrar identidad de beneficiarios. |
| H12 | Mapa agregado | Mostrar sectores con conteos agregados (atendidos/pendientes), sin puntos individuales. Actualización en tiempo real. |

---

## Arquitectura inicial

> Cómo se conectan las partes (interfaz, lógica, Stellar) y en qué punto entra la red. Diagrama simple.

**Componentes:**

1. **Interfaz de usuario (Frontend):**
   - Web responsive para empresas, fundaciones y veedores.
   - Interfaz móvil simplificada para centros de acopio y líderes comunitarios.
   - Tarjeta física o SMS para personas vulnerables (sin app, sin smartphone).

2. **Lógica de negocio (Backend):**
   - API REST que recibe registros de lotes, entradas, salidas y atenciones.
   - Base de datos relacional para datos operativos (usuarios, roles, inventarios, códigos anónimos).
   - Módulo de anonimización: separa identidad real del código público.
   - Módulo de firma: genera hash de cada evento y lo envía a Stellar.

3. **Capa Stellar:**
   - Cada evento crítico (donación firmada, entrada, salida, entrega, atención) genera un hash.
   - El hash se ancla en Stellar mediante una transacción con `memo`.
   - El `transaction_hash` se guarda en la base de datos y se expone en el tablero público.
   - Se usa **multisig** para eventos críticos (empresa + centro de acopio).

4. **Tablero público:**
   - Consulta la base de datos para mostrar estado de lotes.
   - Verifica el hash en Stellar para confirmar que no fue alterado.
   - No muestra datos personales de beneficiarios.

**Diagrama:**

<img width="639" height="322" alt="image" src="https://github.com/user-attachments/assets/630a01f5-f4cb-40f7-a9c9-90df35e68df9" />


**Punto donde entra la red:** en cada evento crítico, el backend calcula un hash de los datos mínimos (ID lote, tipo de evento, fecha, actor) y lo ancla en Stellar. La red no almacena datos personales; solo el hash que prueba que el registro existió y no fue alterado.

---

## Uso de Stellar y justificación

> Qué componentes de Stellar usaría y por qué cada uno. Apoyado en el criterio de pertinencia del Problem Brief.

**Componentes de Stellar que se usarían:**

1. **Transacciones con `memo` (texto o hash):**
   Cada evento crítico (donación firmada, entrada en acopio, salida, entrega, atención) se registra como una transacción en Stellar con un `memo` que contiene el hash del evento. Esto permite anclar el registro sin almacenar datos personales en la red. **¿Por qué?** Porque el `memo` es inmutable y verificable públicamente, y no requiere almacenar datos sensibles en la blockchain.

2. **Cuentas Stellar por actor:**
   Cada empresa, fundación, centro de acopio o líder comunitario tiene una cuenta Stellar. Esto permite asociar cada transacción a un actor verificable y habilita la firma digital (historia H4). **¿Por qué?** Porque permite que cada actor tenga una identidad criptográfica sin necesidad de un registro central de identidades.

3. **Firmas múltiples (multisig):**
   Para eventos críticos, se puede requerir la firma de dos actores (por ejemplo, empresa + centro de acopio) antes de que la
