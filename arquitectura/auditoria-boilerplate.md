# Auditoría del proyecto de referencia

## Alcance

La revisión contrasta la arquitectura propuesta con el estado descrito del prototipo MotoYa. No se recibió en este repositorio el código privado de la aplicación, por lo que no se presentan ejecuciones locales ni resultados de pruebas como si hubieran sido verificados aquí.

## Correspondencia reportada

| Área | Estado conocido | Implicación arquitectónica |
|---|---|---|
| App pasajero | Flujo de registro, mapa, búsqueda, ofertas, viaje, chat, SOS y perfil disponible con simuladores. | Presentación y flujo están adelantados; falta reemplazar simuladores por adaptadores reales. |
| App conductor | Solicitudes, navegación, PIN, espera, cierre, saldo, recarga y registro parcialmente disponibles. | Debe centralizarse la autoridad de dinero y estados antes de producción. |
| Firebase | Pendiente de conexión completa. | Reglas, índices, Functions, App Check y entornos separados son trabajo crítico. |
| Panel de soporte | Pendiente. | Bloquea revisión documental, recargas, atención SOS y gobierno operativo real. |
| Mapas alternativos | Pendientes como respaldo propio. | El puerto debe existir desde el inicio aunque el segundo adaptador llegue después. |
| Pruebas | Se informa una suite automatizada en el proyecto privado. | Debe verificarse en CI y ampliarse con reglas de seguridad, concurrencia e idempotencia. |

## Riesgos encontrados

1. Mientras los conductores y viajes sean simulados en el teléfono, no existe evidencia de seguridad ni concurrencia real.
2. Conectar Firestore sin reglas de denegación por defecto permitiría exposición o modificación de datos.
3. El panel no es accesorio: forma parte del control de conductores, dinero, SOS, reclamos y sanciones.
4. La comisión y el saldo deben migrar a transacciones del servidor antes de usar dinero real.
5. Las métricas de rendimiento, consumo y disponibilidad requieren un piloto instrumentado.

## Criterios de aceptación técnica

- Dominio y casos de uso se prueban sin Firebase ni Google Maps.
- Las reglas de Firestore impiden leer datos de otro usuario y escribir campos críticos.
- Dos pasajeros no pueden asignar al mismo conductor de manera simultánea.
- Repetir el cierre de un viaje no descuenta otra comisión.
- Un corte de red recupera el viaje activo sin crear otro.
- Un SOS persistido aparece en el panel y escala cuando no recibe atención.
