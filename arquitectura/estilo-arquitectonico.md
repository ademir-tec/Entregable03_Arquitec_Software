# Estilo arquitectónico de MotoYa

## Estilo seleccionado

MotoYa combina **cliente-servidor**, **serverless orientado a eventos** y **tiempo real**. Flutter y el panel web son clientes; Firebase proporciona servicios administrados; Cloud Functions ejecuta reglas confiables cuando recibe comandos o cambios persistidos.

El estilo serverless define el despliegue. Clean Architecture organiza el código. Los eventos y suscripciones permiten que pasajero, conductor y soporte observen un viaje sin consultas continuas.

## Componentes y relaciones

[![Arquitectura general de MotoYa](marketplace-arquitectura.png)](marketplace-arquitectura.png)

La [versión interactiva](marketplace-arquitectura.html) se descarga y abre en un navegador. También se conserva la versión Mermaid en [arquitectura inicial](arquitectura-inicial.md#diagrama-de-arquitectura).

## Responsabilidades

| Elemento | Responsabilidad |
|---|---|
| App Flutter | Modos pasajero y conductor, GPS, permisos y estado visual. |
| Panel web | Revisión, incidentes, configuración y reportes por rol. |
| Firebase Auth/App Check | Identidad y aplicación legítima. |
| Firestore | Estado y cambios en tiempo real. |
| Cloud Functions | Tarifas, transiciones, saldos, sanciones y eventos. |
| Storage | Documentos y evidencias privadas. |
| FCM/SMS | Push, verificación y emergencia. |
| Adaptadores de mapas | Google Maps y proveedores alternativos. |

## Relación con los drivers

| Driver | Respuesta |
|---|---|
| DA01, DA04 | Estado persistente, suscripciones y reconexión. |
| DA02, DA03, DA09 | Funciones confiables, auditoría y respuesta operativa. |
| DA05 | Puertos de mapas y respaldo. |
| DA06 | Servicios administrados y escalamiento por demanda. |
| DA07 | Acceso contextual, almacenamiento privado y retención. |
| DA08 | Capas y adaptadores reemplazables. |

## Alternativas evaluadas

| Alternativa | Evaluación |
|---|---|
| Backend Node.js propio | Da control, pero añade servidores, WebSocket y operación antes de validar el piloto. |
| Acceso directo desde Flutter | Reduce código, pero expone dinero y estados a clientes modificados. |
| Firebase serverless | Cubre tiempo real y bajo costo inicial; requiere controlar consumo y acoplamiento. |
| Solo Google Maps | Simplifica el inicio, pero no cubre fallas o incrementos de costo. |
