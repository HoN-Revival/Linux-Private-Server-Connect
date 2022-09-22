# Linux Private Server Connect

This repo contains isntructions on how to connect a HoN Linux client to a custom HoN server.

## Custom Servers

To connect to custom servers, you'll need to pass some command line flags to your application.

```
-masterserver <address> -webserver <address> -messageserver <address>
```

Where the `<address>` is in the form of `<IP>:<port>` or `<IP>` or `<URL>` or `<URL>:<port>`.
    
The default port (if unspecified) is the default HTTP port of `80`.

The easiest way to do this is to edit the `hon.sh` file that you use to launch the game.

Simply update the last line of `hon.sh` script to:

```
exec $exe "$*" -masterserver <masterServer> -webserver <webServer> -messageserver <messageServer>
```

## Project Kongor

To connect to Project Kongor, you can just use this command which is constructed with the appropriate addresses:

```
exec $exe "$*" -masterserver api.kongor.online -webserver api.kongor.online -messageserver api.kongor.online
```
