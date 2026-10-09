# Decisiones arquitectónicas

| ADR | Decisión | Drivers | Estado |
|---|---|---|---|
| ADR-001 | Arquitectura cliente-servidor serverless con Firebase. | DA01, DA04, DA06 | Aceptada |
| ADR-002 | Clean Architecture y puertos/adaptadores. | DA05, DA08 | Aceptada |
| ADR-003 | Autoridad de negocio en Cloud Functions. | DA02, DA03, DA09 | Aceptada |
| ADR-004 | Firestore para estado y actualizaciones en tiempo real. | DA01, DA04, DA06 | Aceptada |
| ADR-005 | Google Maps principal con respaldo intercambiable. | DA05, DA08 | Aceptada |
| ADR-006 | Seguridad por capas y acceso contextual. | DA02, DA07, DA09 | Aceptada |

## ADR-001: backend administrado y serverless

**Contexto.** El MVP necesita autenticación, tiempo real, archivos, notificaciones y lógica confiable con un equipo reducido.

**Decisión.** Usar Firebase Auth, Firestore, Storage, Cloud Functions, Cloud Messaging y Hosting, sin servidor permanente para el flujo principal.

**Consecuencias.** Reduce operación inicial y escala por demanda. Aumenta dependencia del proveedor y exige controlar costos, índices, observabilidad, idempotencia y copias.

## ADR-002: Clean Architecture

**Contexto.** Flutter, Firebase, Google Maps y alternativas pueden cambiar sin alterar reglas.

**Decisión.** Separar Presentación, Aplicación, Dominio e Infraestructura. Los casos de uso consumen contratos internos y la tecnología se conecta mediante adaptadores.

**Consecuencias.** Facilita simuladores y pruebas; añade interfaces, mapeos y composición explícita.

## ADR-003: servidor como autoridad

**Contexto.** El teléfono está bajo control del usuario y puede modificarse.

**Decisión.** Calcular tarifas, comisión, saldo, recargos, advertencias y rangos en funciones confiables. Cada transición valida estado previo, identidad, ubicación, tiempo e idempotencia.

**Consecuencias.** Protege dinero y estados; las funciones deben tolerar reintentos y registrar decisiones.

## ADR-004: modelo reactivo en Firestore

**Contexto.** Pasajero, conductor y panel observan el mismo servicio.

**Decisión.** Persistir el estado operacional en documentos con oyentes en tiempo real y usar transacciones para asignación y saldo.

**Consecuencias.** Simplifica sincronización y reconexión, pero obliga a controlar lecturas, índices y bucles de eventos.

## ADR-005: mapas reemplazables

**Contexto.** Google ofrece un inicio rápido, pero su costo y disponibilidad pueden cambiar.

**Decisión.** Definir contratos de rutas y geocodificación. Google es principal; GraphHopper y Photon son respaldo. El servidor confirma la distancia usada para la tarifa.

**Consecuencias.** Cambiar proveedor no modifica pantallas ni casos de uso. Se registra qué proveedor y ruta sustentaron cada precio.

## ADR-006: seguridad y privacidad por capas

**Contexto.** Ubicaciones, documentos, conversaciones y acciones del panel son sensibles.

**Decisión.** Aplicar App Check, autenticación, autorización contextual, denegación por defecto, enlaces temporales, segundo factor, cifrado, retención y auditoría.

**Consecuencias.** Limita la exposición y facilita investigaciones, pero exige revisar permisos y probar restauración e incidentes.
