# Plan de pruebas

| Nº | Caso | Cómo se prueba | Resultado esperado | Resultado obtenido | Evidencia |
|---|---|---|---|---|---|
| T1 | Monitor, ciclo completo | Ejecutar 01 manualmente | 6 filas en checks: 2 OK, 1 DEGRADADO, 3 CAÍDO | | |
| T2 | Reintentos | Revisar Executions de dominio-roto | 3 intentos; el 503 no se reintenta | | |
| T3 | Anti-spam | Activar 01 y esperar 3 ciclos | 4 avisos en el primero, 0 en el segundo y el tercero | | |
| T4 | Recuperación | Cambiar la URL de api-503 por una válida | 1 aviso [RECUPERADO] | | |
| T5 | API sin clave | curl sin cabecera X-API-Key | 403 | | |
| T6 | API con datos inválidos | severidad "urgente" y descripcion "corta" | 400 con 2 errores | | |
| T7 | API con usuario inexistente | reportado_por: 99 | 422 | | |
| T8 | API válida, severidad media | Petición correcta | 201, vence a 24 h, fila nueva, sin correo | | |
| T9 | API válida, severidad crítica | Petición correcta | 201, vence a 4 h, fila nueva y correo | | |
| T10 | Informe con datos | Ejecutar 04 tras varios ciclos | Correo con 6 filas y CSV adjunto | | |
| T11 | Informe sin datos | Ejecutar 04 con hojas vacías | Correo con «Sin datos», sin error | | |
| T12 | Error global | Nodo Code con throw new Error | Correo [ERROR n8n] con workflow y nodo | | |
