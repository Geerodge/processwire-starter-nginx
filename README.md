# Docker for ProcessWire

Running all the required php extentions for ProcessWire and also the following:

* PHP 7.4
* NGINX
* ImageMagick

## Installation

Clone the [ProcessWire](https://github.com/processwire/processwire) repository.
```
git clone https://github.com/processwire/processwire.git app/public
```

Now run docker compose command and you are good to go.

```
docker-compose up
```

The docker container where ProcessWire is installed can be accessed via 127.0.0.1, visit here in your browser to start the ProcessWire installation.

Information about the mysql connection you can find in `docker-compose.yml`.
