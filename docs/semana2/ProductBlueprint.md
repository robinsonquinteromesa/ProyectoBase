# Product Blueprint — Horizonte Vivo

## Priorización de historias

> Historias elegidas entre las que propuso el equipo y criterio con que se priorizaron. Son las que pasan al backlog.

El equipo reunió **35 historias de usuario** (7 por integrante) y priorizó **12** para el MVP, usando tres criterios:

1. **Impacto directo en el problema raíz:** historias que sin ellas el sistema no funciona (registro de personas vulnerables, registro de salida de lotes, anclaje inalterable).
2. **Habilitadoras de otras historias:** historias que desbloquean el resto de la cadena (registro previo, firma digital, identificador único).
3. **Valor verificable para el usuario final:** historias que producen evidencia concreta para donantes, veedores o beneficiarios.

**Historias priorizadas para el MVP:**

| # | Historia | Autor | Criterio |
|---|---|---|---|
| H1 | Registrar personas vulnerables con sus necesidades | Santiago | Impacto raíz |
| H2 | Registrar salida de lote hacia beneficiario | Gustavo | Impacto raíz |
| H3 | Anclar cada donación en registro público e inalterable | Robinson | Habilitadora técnica |
| H4 | Firma digital de la donación al entregarla | Robinson | Habilitadora técnica |
| H5 | Identificador único por lote en Stellar | Robinson | Habilitadora técnica |
| H6 | Registrar entrada de lote en centro de acopio | Sebastián / Gustavo | Cadena logística |
| H7 | Registrar salida de lote clasificado (reciclable, orgánico, textil) | Sebastián | Cadena ambiental |
| H8 | Consultar tablero público de donaciones entregadas | Gustavo | Valor verificable |
| H9 | Registrar atención a persona vulnerable (alimento, abrigo) | Ricardo | Valor social |
| H10 | Reporte agregado de donaciones recibidas y entregadas | Gustavo | Transparencia |
| H11 | Verificar cadena completa sin datos personales | Robinson | Auditoría |
| H12 | Mapa de personas vulnerables atendidas y pendientes | Santiago | Coordinación territorial |

Las restantes quedan como **backlog deseable** para versiones posteriores.

## Propuesta de valor

> Qué resultado obtiene el usuario y por qué elegiría esta solución. En qué se diferencia de cómo resuelve hoy. Conecta con el usuario del Problem Brief.

Horizonte Vivo le entrega a cada actor una **prueba verificable de que su aporte llegó a destino**, sin depender de la palabra de nadie. Para el **donante empresarial**, significa que puede ver en un tablero público que su donación fue registrada como entregada, y obtener una certificación verificable para posibles beneficios tributarios. Para la **persona mayor sin pensión o en situación de calle**, significa dejar de ser invisible: tendrá un historial de atenciones que responde por ella incluso cuando nadie cercano puede hacerlo. Para la **fundación o iglesia**, significa poder demostrar transparencia ante donantes y cooperación internacional con reportes generados automáticamente desde el registro. Para el **veedor comunitario o periodista**, significa poder auditar entradas y salidas de un centro de acopio sin acceder a datos personales de beneficiarios.

Hoy todo esto se resuelve con WhatsApp, papel, fotos y buena voluntad, y el costo es que nadie puede verificar nada: ni el donante sabe si su aporte llegó, ni la persona vulnerable tiene cómo probar que fue atendida, ni la fundación tiene cómo defenderse de una sospecha. La diferencia es que Horizonte Vivo **no reemplaza la logística, le agrega trazabilidad inalterable**. El usuario no cambia su forma de donar ni de atender; cambia la posibilidad de probar lo que hizo.

## Flujo de usuario

> Recorrido de la persona por la solución de principio a fin, roles y puntos de interacción. Diagrama o secuencia numerada.

**Flujo principal (donación de alimentos en emergencia):**

1. **Empresa donante** entra a la app y registra un lote: categoría (alimento), cantidad, fecha, destino previsto. → Genera identificador único.
2. **Empresa** firma digitalmente el registro con su clave Stellar. → El lote queda anclado en la red.
3. **Centro de acopio** recibe el lote y registra la entrada con el identificador único. → Se vincula al mismo hash.
4. **Centro de acopio** clasifica y registra la salida hacia un grupo o familia beneficiaria.
5. **Líder comunitario** registra la entrega final, vinculando el lote a un código anónimo de beneficiario.
6. **Persona vulnerable** recibe el alimento y, si tiene tarjeta o código, puede verificar que fue registrada.
7. **Donante** consulta el tablero público y ve: lote #X → entregado en fecha Y → destino Z (sin datos personales).
8. **Veedor o periodista** consulta reporte agregado del centro de acopio: entradas vs. salidas, sin datos personales.
9. **Fundación** genera reporte automático para sus donantes o cooperación internacional.

**Roles y puntos de interacción:**
- Empresa → interfaz web: registrar y firmar lote.
- Centro de acopio → interfaz móvil: registrar entrada/salida.
- Líder comunitario → interfaz móvil simplificada: registrar entrega.
- Persona vulnerable → tarjeta física o SMS: verificar atención.
- Donante/veedor → tablero público web: consultar estado.

## Alcance del MVP

> Funcionalidad central separada de la deseable que queda fuera. Justificación de por qué el recorte sigue entregando valor.

**Dentro del MVP (funcionalidad central):**
- Registro de lotes de donación (categoría, cantidad, fecha, origen).
- Firma digital de la donación por parte de la empresa.
- Anclaje en Stellar del hash de cada lote con identificador único.
- Registro de entrada en centro de acopio.
- Registro de salida hacia beneficiario o transformador.
- Registro de personas vulnerables con código anónimo.
- Registro de atención (alimento, abrigo, visita).
- Tablero público de donaciones entregadas (sin datos personales).
- Reporte agregado por centro de acopio.
- Verificación de cadena completa por hash público.

**Fuera del MVP (deseable):**
- Mapa interactivo de huertas y puntos de acopio.
- Certificación automática de beneficios tributarios.
- Integración con sistemas de gobierno (UNGRD, INVIMA).
- Módulo de manufactura textil y compost comercial.
- App nativa móvil (el MVP puede ser web responsive).
- Verificación por SMS en zonas sin internet.
- Módulo de protección animal.

**Justificación del recorte:** El MVP se enfoca en **una sola cadena completa** —donación de alimentos en emergencia, desde la empresa hasta la persona vulnerable— porque es la que responde al contexto del terremoto y al problema raíz del Problem Brief. Con esta cadena funcionando de extremo a extremo, el sistema ya entrega valor verificable: el donante ve impacto, el centro de acopio se protege, la persona vulnerable deja de ser invisible y el veedor puede auditar. Lo deseable (mapas, certificaciones, integraciones, otras cadenas) se puede construir encima sin rediseñar el núcleo.

## Lean Canvas

> Lienzo de una página con el modelo del producto.

| Bloque | Contenido |
|---|---|
| **Problema** | Donaciones sin trazabilidad; personas vulnerables invisibles; donantes sin evidencia de impacto; fundaciones sin transparencia demostrable. |
| **Segmento de usuarios** | Empresas donantes; fundaciones e iglesias; centros de acopio; líderes comunitarios; personas mayores sin pensión, en calle o en abandono; damnificados del terremoto. |
| **Propuesta de valor única** | Prueba verificable de que cada donación llegó a destino, sin exponer datos personales de los beneficiarios. |
| **Solución** | App web/móvil + anclaje en Stellar + tablero público + tarjetas/códigos anónimos para beneficiarios. |
| **Canales** | Alianzas con fundaciones, iglesias, colegios, universidades y empresas; redes comunitarias; GitHub como repositorio público. |
| **Métricas clave** | % de donaciones registradas con trazabilidad completa; tiempo promedio entre donación y entrega verificada; número de personas vulnerables registradas; número de auditorías ciudadanas realizadas. |
| **Ventaja diferencial** | No reemplaza la logística, la vuelve auditable. Registro inalterable + protección de datos + foco en emergencias + diseño para población vulnerable. |
| **Estructura de costos** | Desarrollo y mantenimiento de la plataforma; comisiones de red Stellar (muy bajas); capacitación y acompañamiento comunitario; logística de tarjetas/códigos. |
| **Fuentes de ingresos** | Convenios con empresas (RSE + certificación); convenios con fundaciones y cooperación internacional; servicios de reporte para auditoría; venta de compost y productos textiles (fase posterior). |

**Enlace al Lean Canvas (imagen):** [Pendiente de subir a `/docs/semana2/lean-canvas.png`]

## Backlog priorizado (Kanban)

> Enlace al tablero en GitHub Projects, construido con las historias priorizadas, en columnas y con criterios de aceptación por tarjeta.

**Enlace al tablero:** `https://github.com/users/Andruw5/projects/[número]` (reemplazar con el enlace real del equipo)

**Columnas:** Backlog → Ready → In Progress → In Review → Done

**Criterios de aceptación por historia (ejemplos):**

- **H1 (Registrar personas vulnerables):** Debe permitir crear ficha con código anónimo, necesidades básicas y sector. No debe mostrar nombre completo en vistas públicas.
- **H2 (Registrar salida de lote):** Debe permitir elegir lote existente, tipo de beneficiario (grupo/familia/persona) y fecha. Debe generar hash y anclarlo.
- **H3 (Anclar en Stellar):** Cada registro debe tener un `transaction_hash` verificable en un explorador de Stellar.
- **H4 (Firma digital):** La empresa debe poder firmar con su clave; el sistema debe rechazar registros sin firma.
- **H5 (Identificador único):** Cada lote debe tener un ID único e inmutable, consultable desde el tablero público.
- **H6 (Registrar entrada en acopio):** Debe vincular el lote al hash original y registrar fecha/hora/responsable.
- **H7 (Registrar salida clasificada):** Debe permitir seleccionar tipo (reciclable, orgánico, textil) y destino.
- **H8 (Tablero público):** Debe mostrar estado del lote sin datos personales; debe ser accesible sin login.
- **H9 (Registrar atención):** Debe permitir registrar tipo de atención, fecha y responsable; no debe exponer identidad.
- **H10 (Reporte agregado):** Debe generar PDF/CSV con entradas vs. salidas por periodo.
- **H11 (Verificar cadena sin datos personales):** Debe permitir consultar por hash y mostrar el recorrido completo.
- **H12 (Mapa de personas vulnerables):** Debe mostrar sectores con conteos agregados, sin puntos individuales.

## Arquitectura inicial

> Cómo se conectan las partes (interfaz, lógica, Stellar) y en qué punto entra la red. Diagrama simple.

**Componentes:**

1. **Interfaz de usuario (Frontend):**
   - Web responsive para empresas, fundaciones y veedores.
   - Interfaz móvil simplificada para centros de acopio y líderes comunitarios.
   - Tarjeta física o SMS para personas vulnerables (sin app).

2. **Lógica de negocio (Backend):**
   - API REST que recibe registros de lotes, entradas, salidas y atenciones.
   - Base de datos relacional para datos operativos (usuarios, roles, inventarios).
   - Módulo de anonimización: separa identidad real del código público.

3. **Capa Stellar:**
   - Cada evento crítico (donación firmada, entrada, salida, entrega) genera un hash.
   - El hash se ancla en Stellar mediante una transacción con `memo`.
   - El `transaction_hash` se guarda en la base de datos y se expone en el tablero público.

4. **Tablero público:**
   - Consulta la base de datos para mostrar estado de lotes.
   - Verifica el hash en Stellar para confirmar que no fue alterado.
   - No muestra datos personales de beneficiarios.

**Diagrama (secuencia):**
