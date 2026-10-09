# 05. Restricciones

| ID | Restricción | Consecuencia arquitectónica |
|---|---|---|
| RC01 | Android es la primera plataforma; iOS corresponde a una fase posterior. | Flutter comparte código y prioriza validación en Android. |
| RC02 | Una sola app cambia entre pasajero y conductor. | Identidad común con permisos y navegación por modo. |
| RC03 | El pago del viaje ocurre fuera de MotoYa mediante efectivo, Yape o Plin. | No se almacenan tarjetas ni se confirma el pago del viaje. |
| RC04 | Soporte confirma manualmente las recargas del conductor. | Cola, evidencia, código único y movimientos auditables. |
| RC05 | La zona inicial es Huamanga. | Origen, destino y búsqueda se validan contra zonas configurables. |
| RC06 | La conectividad móvil puede ser irregular. | Estado persistente, reconexión y operaciones idempotentes. |
| RC07 | Rutas y direcciones dependen de servicios externos. | Puertos, adaptadores, límites de consumo y respaldo. |
| RC08 | El panel no tiene registro abierto y exige segundo factor. | Cuentas creadas por personal autorizado y sesiones breves. |
| RC09 | Se tratan DNI, documentos, ubicación y conversaciones. | Minimización, cifrado, almacenamiento privado y retención. |
| RC10 | El teléfono no decide tarifas, saldos, sanciones ni estados críticos. | Lógica confiable en Cloud Functions. |
| RC11 | Alertas de seguridad y viaje no pueden desactivarse. | Preferencias limitadas a promociones y novedades. |
| RC12 | GitHub no almacena claves. | Secretos fuera del repositorio y gestionados por el entorno. |

## Fuera del MVP

- Pagos del viaje dentro de la aplicación.
- Mototaxis de tres ruedas, paquetes y otras ciudades.
- Viajes programados.
- Sanciones definitivas totalmente automáticas.
