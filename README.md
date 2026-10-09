# MotoYa — Arquitectura de Software

## Integrante

Alvaro Ademir Ayala Arango.

## Descripción

MotoYa es una aplicación móvil de moto lineal como taxi para Huamanga, Ayacucho. Conecta pasajeros con conductores verificados, permite negociar la tarifa antes de asignar el viaje y registra el servicio con PIN de inicio, seguimiento, contactos de emergencia y SOS.

El pasajero paga directamente al conductor mediante efectivo, Yape o Plin. MotoYa cobra al conductor una comisión de su saldo prepagado cuando termina un viaje.

## Alcance

- Una aplicación Flutter con modo pasajero y modo conductor.
- Panel web para soporte, administración, dueño y contador.
- Solicitud, negociación, asignación y seguimiento de viajes en tiempo real.
- Registro documental de conductores y motos.
- Saldo, recargas verificadas y cobro de comisiones.
- Chat, SOS, calificaciones, reclamos, sanciones y auditoría.
- Google Maps Platform con proveedores alternativos de respaldo.

Quedan fuera del MVP los pagos del viaje dentro de la aplicación, los mototaxis de tres ruedas, los envíos de paquetes, los viajes programados y otras ciudades.

## Estructura

```text
Entregable03_Arquitec_Software/
├── analisis-de-sistema/
│   ├── 01-actores.md
│   ├── 02-historias-del-usuario.md
│   ├── 03-requisitos-funcionales.md
│   ├── 04-atributos-de-calidad.md
│   ├── 05-restricciones.md
│   └── 06-driver-arquitectonicos.md
├── arquitectura/
│   ├── enfoque/
│   ├── arquitectura-inicial.md
│   ├── auditoria-boilerplate.md
│   ├── decisiones-arquitectonicas.md
│   ├── estilo-arquitectonico.md
│   └── README.md
├── .gitignore
└── README.md
```

## Entregables

| Tema | Documento |
|---|---|
| Actores | [Actores y límites](analisis-de-sistema/01-actores.md) |
| Historias | [Historias de usuario](analisis-de-sistema/02-historias-del-usuario.md) |
| Funciones | [Requisitos funcionales](analisis-de-sistema/03-requisitos-funcionales.md) |
| Calidad | [Atributos de calidad](analisis-de-sistema/04-atributos-de-calidad.md) |
| Restricciones | [Restricciones](analisis-de-sistema/05-restricciones.md) |
| Drivers | [Drivers arquitectónicos](analisis-de-sistema/06-driver-arquitectonicos.md) |
| Diseño | [Arquitectura inicial](arquitectura/arquitectura-inicial.md) |
| Decisiones | [Decisiones arquitectónicas](arquitectura/decisiones-arquitectonicas.md) |
| Estilo | [Estilo arquitectónico](arquitectura/estilo-arquitectonico.md) |
| Enfoque | [Clean Architecture](arquitectura/enfoque/enfoque-arquitectonico.md) |
