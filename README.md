# Balanceo web con HAProxy y Apache en Docker

Escenario contenerizado para practicar balanceo de carga usando HAProxy como proxy inverso y varios servidores Apache como backends.

## Objetivo

El objetivo del proyecto es desplegar un entorno sencillo de balanceo web con Docker Compose, simulando una arquitectura donde HAProxy distribuye el tráfico entre varios servidores Apache.
Este proyecto permite practicar conceptos básicos de alta disponibilidad, proxy inverso, balanceo de carga y despliegue de servicios web mediante contenedores.

## Arquitectura

```text
Cliente
  │
  ▼
HAProxy
  ├── Apache 1
  ├── Apache 2
  └── Apache 3
```

## Tecnologías utilizadas

- Docker
- Docker Compose
- HAProxy
- Apache
- HTML
- Redes Docker

## Estructura del proyecto

```text
.
├── apache/
│   └── Configuración y contenido web de Apache
├── haproxy/
│   └── Configuración de HAProxy
├── Dockerfile
├── docker-compose.yml
└── README.md
```

## Funcionamiento

HAProxy recibe las peticiones HTTP y las reparte entre los contenedores Apache disponibles.

Cada servidor Apache actúa como backend, permitiendo comprobar cómo se distribuye el tráfico entre distintos servicios web.

## Ejecución

Para levantar el entorno:

```bash
docker compose up -d
```

Para comprobar los contenedores activos:

```bash
docker ps
```

Para ver los logs:

```bash
docker compose logs -f
```

Para detener el entorno:

```bash
docker compose down
```

## Qué demuestra este proyecto

- Configuración básica de HAProxy.
- Despliegue de múltiples servidores web con Docker.
- Balanceo de carga entre contenedores Apache.
- Uso de Docker Compose para levantar una arquitectura completa.
- Comprensión de conceptos de proxy inverso y alta disponibilidad.

## Próximas mejoras

- Añadir healthchecks.
- Añadir métricas básicas de HAProxy.
- Documentar pruebas de balanceo.
- Añadir HTTPS.
- Añadir un diagrama de arquitectura.
Añadir healthchecks.
Añadir métricas básicas de HAProxy.
Documentar pruebas de balanceo.
Añadir HTTPS.
Añadir un diagrama de arquitectura.
