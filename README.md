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

## Estructura

```text
src/main/java/com/icesi/buscaminas/
├── client/
│   ├── BuscaminasClient.java
│   └── BuscaminasSwingClient.java
├── game/
│   ├── ActionResult.java
│   ├── GameSelfTest.java
│   ├── GameStatus.java
│   └── MinesweeperGame.java
├── protocol/
│   └── Protocol.java
└── server/
    ├── BuscaminasServer.java
    └── ClientHandler.java
```

## Requisitos

- JDK 17 o superior.
- IntelliJ IDEA recomendado.

## Ejecución en IntelliJ IDEA

1. Abrir la carpeta del proyecto en IntelliJ IDEA.
2. Configurar un JDK 17 o superior en `File > Project Structure > Project SDK`.
3. Ejecutar primero:

```text
com.icesi.buscaminas.server.BuscaminasServer
```

4. Ejecutar después el cliente gráfico:

```text
com.icesi.buscaminas.client.BuscaminasSwingClient
```

También puede ejecutarse el cliente de consola:

```text
com.icesi.buscaminas.client.BuscaminasClient
```

Para comprobar la concurrencia se pueden abrir varias instancias del cliente mientras el servidor permanece ejecutándose.

## Comandos del protocolo

```text
NUEVO
NUEVO 12 12 20
ABRIR 3 4
BANDERA 5 2
TABLERO
ESTADO
AYUDA
SALIR
```

El servidor finaliza cada respuesta con la línea `END`, utilizada como delimitador de mensajes.

## Compilación con Maven

```bash
mvn compile
```

Servidor:

```bash
java -cp target/classes com.icesi.buscaminas.server.BuscaminasServer
```

Cliente gráfico:

```bash
java -cp target/classes com.icesi.buscaminas.client.BuscaminasSwingClient
```
