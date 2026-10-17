# MVP Functional — Horizonte Vivo

**Repositorio:** `(https://github.com/robinsonquinteromesa/ProyectoBase)`
**Video de demostración:** `https://youtube.com/watch?v=[ID]`
**Contract ID (Testnet):** `C...`
**Enlace de transacción de ejemplo:** `(https://stellarapex.org/projects/09a6ed2a-e39f-4fd0-98f3-b83e9c5914b0)`
**URL del producto:** `(https://horizontevivo.org/)`

---

## Aprendizajes y ajustes priorizados

Durante la implementación del MVP, el equipo aprendió principalmente tres cosas. Primero, **el costo de escritura on-chain es extremadamente bajo pero el flujo de firma es engorroso**: cada registro de lote requiere que el donante firme con su wallet; en el contexto de donaciones en emergencia, los donantes empresariales pueden no estar dispuestos a operar personalmente, por lo que en el futuro se necesitará un modelo de "firma en nombre" o "firma múltiple". Segundo, **la experiencia de usuario de protección de privacidad debe diseñarse tempranamente**: inicialmente planeamos escribir el ID del destinatario on-chain, pero luego descubrimos que esto viola los requisitos de privacidad del Problem Brief, por lo que lo cambiamos a "off-chain guardar identidad real + on-chain solo almacenar lot_id y estado", lo que aumenta la complejidad del backend pero es un compromiso necesario para proteger a las personas vulnerables.

En cuanto a ajustes priorizados (ordenados por impacto × esfuerzo):

| Prioridad | Ajuste | Impacto | Esfuerzo |
|---|---|---|---|
| P0 | Añadir mecanismo de reintento de fallos en llamadas al contrato (si falla la red o la wallet rechaza) | Alto | Bajo |
| P0 | Añadir validación backend para lot_id para prevenir registros duplicados | Alto | Bajo |
| P1 | Añadir página de consulta pública de "verificar por lot_id" (sin necesidad de login) | Alto | Medio |
| P2 | Añadir generación de código QR para que donantes generen identificación de lote con un clic | Medio | Medio |
| P3 | Integrar notificaciones por SMS (para personas vulnerables sin smartphones) | Alto | Alto (requiere proveedor externo) |

Antes del cierre de esta semana se completan los dos ítems P0; los P1 y P2 se completan si hay tiempo; P3 queda pendiente para la próxima fase.

---

## Riesgos y pendientes

**Riesgo 1: Gestión de claves de wallet.** Actualmente el frontend depende de la firma de wallet (Freighter/xBull). Si un donante pierde su clave o la wallet no es compatible, no puede completar el registro on-chain. **Mitigación**: en el corto plazo, proporcionar una "cuenta puente" operada por el equipo para que pequeñas donaciones sean firmadas por el equipo en nombre del donante (con su consentimiento); en el largo plazo, explorar la posibilidad de integrar smart wallet o passkey.

**Riesgo 2: Brecha digital para beneficiarios.** El diseño actual asume que el destinatario o el líder comunitario tienen un smartphone para recibir códigos. En comunidades rurales o en situaciones de calle, esto no se cumple. **Pendiente**: diseñar un sistema de "tarjeta física + verificación SMS", pero esto requiere alianzas con operadores de telecomunicaciones, fuera del alcance del MVP actual.

**Riesgo 3: Riesgo legal y de cumplimiento.** Registros on-chain de donaciones pueden involucrar protección de datos (Ley 1581 de Colombia) y certificación tributaria. Actualmente el MVP no almacena datos personales on-chain, pero los términos de privacidad y el aviso legal deben redactarse antes del lanzamiento. **Pendiente**: consultar con asesores legales, confirmar si "hash on-chain + datos off-chain" cumple con los requisitos de protección de datos.

**Riesgo 4: Mantenimiento de la red de testnet.** El MVP está desplegado en testnet; si el testnet se reinicia o hay inestabilidad en el RPC, los datos on-chain pueden perderse. **Pendiente**: antes de pasar a mainnet, implementar estrategia de respaldo de datos off-chain; el MVP actual ya tiene respaldo en la base de datos backend.

**Deuda técnica restante**: el frontend no tiene manejo de errores unificado, la página pública aún no está internacionalizada (español/inglés), el contrato aún no tiene pruebas unitarias. Estos ítems no afectan la demostración del MVP pero deben resolverse antes de la próxima iteración.

---

## Plan de validación con usuarios

**Usuarios objetivo** (del Problem Brief): donantes de empresas (personas de RSE o sostenibilidad), administradores de centros de acopio, coordinadores de ONG/iglesias, trabajadores sociales/líderes comunitarios.

**Método de validación y cronograma:**

**Fase 1: Pruebas de usabilidad (2 semanas después del MVP)**
- **Objeto**: 3-5 administradores de centros de acopio o coordinadores de ONG.
- **Método**: sesiones presenciales de 30 minutos, observar si pueden completar de forma independiente: registrar lote → verificar lote → compartir enlace público.
- **Hipótesis**: "Un usuario no técnico puede completar el registro de un lote en 5 minutos sin capacitación." **Criterio de éxito**: 4/5 usuarios completan la tarea sin ayuda, y expresan que la página pública de verificación "me hace sentir más seguro".

**Fase 2: Entrevistas de seguimiento con donantes (3-4 semanas después del MVP)**
- **Objeto**: 3 empresas que hayan donado recientemente (incluidas las que usaron herramientas de la competencia o métodos tradicionales).
- **Método**: entrevistas semiestructuradas de 20 minutos, enfocadas en: ¿Estarían dispuestos a usar este sistema en la próxima donación? ¿Qué evidencia esperan ver en la "página de verificación"? ¿La certificación tributaria es un factor decisivo?
- **Hipótesis**: "Los donantes están dispuestos a dedicar 2 minutos extra para obtener un registro de trazabilidad verificable." **Criterio de éxito**: al menos 2/3 donantes expresan disposición a usar en la próxima donación, y mencionan espontáneamente "transparencia" o "certificación" como razón.

**Fase 3: Validación de datos (después de acumular 20 lotes)**
- **Indicadores**: porcentaje de lotes con registro on-chain completo (objetivo >90%), tasa de éxito de firma de donantes (objetivo >80%), número de consultas a la página pública (objetivo: al menos 5 consultas por lote en promedio).
- **Hipótesis**: "El registro on-chain no reduce la velocidad de procesamiento de donaciones, y la tasa de consultas públicas demuestra que hay demanda real de trazabilidad."

**Criterios para determinar el éxito**: si las tres fases cumplen los criterios, se considera que la hipótesis central del MVP está validada y se puede pasar a la fase de "integración con ONG reales". Si la Fase 1 falla, priorizar la simplificación del flujo de registro; si la Fase 2 falla, reevaluar el incentivo de certificación para donantes.
