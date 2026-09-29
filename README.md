# Buscaminas con Sockets TCP en Java

Proyecto cliente-servidor de Buscaminas desarrollado en Java usando sockets TCP.

## Características

- Servidor TCP sobre el puerto `8080`.
- Comunicación cliente-servidor con `ServerSocket` y `Socket`.
- Lectura y escritura mediante `BufferedReader` y `PrintWriter`.
- Atención concurrente de varios clientes con `ExecutorService`.
- Una partida independiente por cada cliente conectado.
- Interfaz gráfica con Swing.
- Cliente de consola disponible.
- Manejo de timeouts y cierre seguro de recursos.
