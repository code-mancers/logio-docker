# LogIO-Docker

Forward your Dockerized stack logs to a nice looking browser based UI.

This is a fork of [https://github.com/geniousphp/logio-docker](https://github.com/geniousphp/logio-docker)
that restricts log retrieval only using docker-compose project name.

## Features
* Forward your containers logs to a browser based UI (inspired by [logio](http://logio.org/))
* Show logs in real-time (powered by [socket.io](http://socket.io/))
* Filter containers by label
* Filter within logs
* LogIO-Docker is dockerized and built on Alpine Linux (~40MB)

## Usage as a Container

```
docker run -d -p 28778:28778 -v /var/run/docker.sock:/var/run/docker.sock --name=logio codemancers/logio
```

See it on `http://localhost:28778/#?projectName=<docker-compose project name>`

## UI

![alt tag](https://raw.githubusercontent.com/geniousphp/soam/master/public/ui.png)

## License

MIT
