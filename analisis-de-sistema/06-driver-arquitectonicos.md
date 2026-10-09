# 06. Drivers arquitectónicos

| Driver | Problema que plantea | Decisión que responde |
|---|---|---|
| **DA01 — Tiempo real** | Solicitudes, ofertas, GPS, chat y SOS requieren baja latencia. | Firestore con suscripciones y funciones orientadas a eventos. |
| **DA02 — Seguridad del viaje** | El servicio físico implica riesgo para pasajero y conductor. | Verificación, PIN, SOS, trazabilidad y detección de GPS falso. |
| **DA03 — Integridad del negocio** | Un cliente modificado podría alterar dinero o estados. | Autoridad en servidor, denegación por defecto e idempotencia. |
| **DA04 — Conectividad irregular** | La red puede cortarse durante el viaje. | Estado persistente, reconexión y recuperación desde servidor. |
| **DA05 — Mapas externos** | Rutas y geocodificación dependen de costo y disponibilidad. | Google Maps principal y GraphHopper/Photon como adaptadores de respaldo. |
| **DA06 — Escalabilidad y costo** | El piloto debe iniciar barato y crecer. | Servicios serverless administrados y pago por uso. |
| **DA07 — Privacidad** | Se procesan ubicación, identidad, documentos y chat. | Minimización, cifrado, enlaces temporales y acceso contextual. |
| **DA08 — Mantenibilidad** | Apps, panel y proveedores cambian a ritmos distintos. | Capas, módulos y puertos/adaptadores. |
| **DA09 — Auditoría** | Recargas, sanciones, configuración y SOS requieren responsabilidad. | Historial inmutable y permisos por rol. |

Estas decisiones se representan en la [arquitectura inicial](../arquitectura/arquitectura-inicial.md).
