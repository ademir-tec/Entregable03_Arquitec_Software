# 02. Historias de usuario

| ID | Historia | Criterios de aceptación |
|---|---|---|
| HU01 | Como pasajero, quiero registrarme con mi celular para utilizar MotoYa. | El número se verifica por SMS y no se crean cuentas duplicadas. |
| HU02 | Como pasajero, quiero elegir origen y destino para conocer ruta, tiempo y tarifa. | Los puntos están en la zona; la ruta proviene del servicio configurado; el servidor calcula el monto. |
| HU03 | Como pasajero, quiero proponer una tarifa y comparar ofertas para elegir conductor. | La oferta respeta el rango; se muestran conductor, moto, placa, calificación, llegada y precio. |
| HU04 | Como conductor, quiero recibir solicitudes cercanas para realizar viajes. | Debe estar aprobado, conectado, dentro del radio, con GPS válido y saldo suficiente. |
| HU05 | Como conductor, quiero aceptar o contraofertar para acordar un precio. | Responde una vez por versión de la oferta; la respuesta vence a los 45 segundos. |
| HU06 | Como pasajero, quiero seguir y compartir mi viaje para aumentar mi seguridad. | La ubicación se actualiza durante el viaje y deja de compartirse cuando termina. |
| HU07 | Como usuario, quiero activar SOS para recibir ayuda ante un incidente. | La alerta se persiste, llega a soporte en tiempo real y no puede borrarse. |
| HU08 | Como conductor, quiero registrar mis documentos para demostrar que estoy habilitado. | Se revisan DNI, selfie, licencia, SOAT, TIV y datos de la moto. |
| HU09 | Como agente, quiero revisar registros para admitir conductores verificados. | Aprobar, observar o rechazar exige motivo, notifica y deja auditoría. |
| HU10 | Como conductor, quiero recargar saldo para cubrir las comisiones. | El código de operación es único y soporte confirma el abono antes de acreditarlo. |
| HU11 | Como conductor, quiero iniciar con el PIN del pasajero para confirmar a la persona correcta. | Tras tres intentos fallidos se alerta a soporte; solo el servidor cambia el estado. |
| HU12 | Como pasajero y conductor, quiero chatear para coordinar el recojo. | El chat existe entre asignación y cierre y se conserva noventa días. |
| HU13 | Como pasajero, quiero ver la llegada y el tiempo de espera. | Se valida proximidad, hay cinco minutos gratis y luego recargo configurable. |
| HU14 | Como usuario, quiero calificar y reclamar para construir reputación y resolver problemas. | Solo participantes califican; el reclamo conserva evidencia y estado. |
| HU15 | Como administrador, quiero sancionar con evidencia para proteger a la comunidad. | Se respeta el límite del rol y otra persona resuelve la apelación. |
| HU16 | Como personal autorizado, quiero usar el panel para atender la operación. | Cada rol ve solo sus módulos; datos sensibles se ocultan y la sesión expira. |
