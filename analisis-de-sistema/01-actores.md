# 01. Actores del sistema

| ID | Actor | Tipo | Interacción principal | Límite de acceso |
|---|---|---|---|---|
| ACT01 | Pasajero | Persona | Solicita, negocia, sigue, comparte y califica viajes. | Solo consulta y modifica su cuenta, solicitudes y viajes. |
| ACT02 | Conductor | Persona | Registra moto y documentos, recibe solicitudes, realiza viajes y recarga saldo. | Trabaja solo con registro aprobado, documentos vigentes y saldo suficiente. |
| ACT03 | Agente de soporte | Persona | Revisa registros y recargas, atiende SOS y reclamos, y aplica medidas limitadas. | Accede a datos sensibles únicamente dentro de un caso; toda acción se audita. |
| ACT04 | Administrador | Persona | Gestiona operación, agentes, sanciones, zonas, avisos y métricas. | No modifica decisiones reservadas al dueño. |
| ACT05 | Dueño | Persona | Controla configuración, finanzas, personal, lista negra y medidas permanentes. | Las acciones críticas exigen segundo factor y motivo. |
| ACT06 | Contador | Persona | Consulta y exporta reportes financieros. | Acceso de solo lectura y sin datos personales operativos. |
| ACT07 | Servicio de mapas | Sistema externo | Proporciona mapas, geocodificación, rutas, distancia y tiempo. | No decide tarifas ni estados del viaje. |
| ACT08 | Servicio de notificaciones | Sistema externo | Envía notificaciones push y códigos SMS. | Recibe únicamente destinatario y contenido mínimo. |

Una persona posee una cuenta por número celular. Puede usar el modo pasajero y, después de una revisión aprobada, el modo conductor. El personal del panel utiliza cuentas separadas sin registro público.
