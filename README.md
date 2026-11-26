# Práctica 2 – Plataforma de monitorización y gestión de incidencias con n8n

Despliegue y Automatización · UCJC · 4º Ingeniería Informática

## Equipo y reparto
- Fernando Melero (FerMelero): entorno, 05-manejador-errores, 02-notificador, 01-monitor-salud.
- Giordano (Giordano-jpg): 03-api-incidencias, 04-informe-diario, enlace de Error Workflow, pruebas y documentación.

## Arranque
```bash
docker compose up -d   # n8n en http://localhost:5678
```
Importar los JSON de `workflows/` y reasignar las credenciales (SMTP, Google Sheets, Header Auth).

## Pendiente de completar
Descripción y diagrama, tablas de nodos, decisiones de diseño, respuestas a las 4 preguntas, problemas encontrados.
