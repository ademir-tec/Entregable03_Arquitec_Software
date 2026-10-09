# 03. Requisitos funcionales

| ID | Requisito funcional | Historia | Módulo |
|---|---|---|---|
| RF01 | Registrar e iniciar sesión por celular verificado; mantener una cuenta con modos pasajero y conductor. | HU01, HU08 | Identidad |
| RF02 | Mostrar ubicación, conductores libres, origen, destino y lugares dentro de la zona. | HU02 | Mapas |
| RF03 | Calcular en servidor ruta, distancia, tiempo y tarifa recomendada. | HU02 | Tarifas y Mapas |
| RF04 | Crear una solicitud con oferta y medio de pago y distribuirla por radios progresivos. | HU03, HU04 | Despacho |
| RF05 | Recibir aceptaciones y contraofertas; asignar exactamente un conductor. | HU03, HU05 | Negociación |
| RF06 | Registrar conductor, moto, selfie y documentos; aprobar, observar o rechazar. | HU08, HU09 | Conductores |
| RF07 | Controlar conexión según aprobación, vigencia, GPS y saldo. | HU04, HU08 | Conductores |
| RF08 | Gestionar estados del viaje desde asignación hasta término o cancelación. | HU04, HU11, HU13 | Viajes |
| RF09 | Exigir PIN para iniciar y validar proximidad para marcar llegada. | HU11, HU13 | Viajes y Seguridad |
| RF10 | Actualizar ubicación en tiempo real y recuperar estado después de un corte. | HU04, HU06 | Seguimiento |
| RF11 | Compartir información mínima y activar SOS manual o automáticamente. | HU06, HU07 | Seguridad |
| RF12 | Mantener chat temporal asociado al viaje. | HU12 | Comunicación |
| RF13 | Calcular espera, recargo, cancelación y advertencias con hora y GPS del servidor. | HU13 | Viajes |
| RF14 | Registrar recargas pendientes, impedir códigos duplicados y acreditar tras revisión. | HU10 | Saldos |
| RF15 | Descontar al terminar la comisión por kilómetro o registrar promoción sin comisión. | HU10 | Saldos y Tarifas |
| RF16 | Registrar calificaciones, reclamos, sanciones, apelaciones y lista negra. | HU14, HU15 | Confianza |
| RF17 | Proporcionar panel con colas de registros, recargas, SOS, reclamos y viajes. | HU09, HU16 | Panel |
| RF18 | Configurar tarifas, comisión, radios, espera, zonas y versión mínima con historial. | HU16 | Configuración |
| RF19 | Aplicar acceso por rol y contexto y revelar datos sensibles solo cuando proceda. | HU16 | Identidad y Auditoría |
| RF20 | Generar métricas operativas y financieras con exportación autorizada. | HU16 | Reportes |

## Reglas críticas

1. Tarifa recomendada: ruta más rápida × S/ 2.14 por km, mínimo S/ 3.00 y S/ 2.00 adicionales de 23:00 a 04:30.
2. La oferta permanece entre 70 % y 200 % de la recomendada; la contraoferta aumenta hasta S/ 3.00 en pasos de S/ 0.50.
3. La búsqueda usa radios de 1.5, 2.5 y 3 km; cada oferta vence a los 45 segundos y la solicitud a los 3 minutos.
4. La comisión es S/ 0.333 por kilómetro planeado y se descuenta solo al terminar.
5. “Llegué” exige estar a 100 m; hay cinco minutos gratis y luego S/ 0.50 por minuto.
6. Un saldo es la suma de movimientos y nunca una cifra editada directamente.
7. Tarifa, comisión, saldo, sanciones y estados críticos se escriben únicamente desde funciones confiables.
