![HTML5 Speedtest Logo](https://github.com/adolfintel/speedtest/blob/master/.logo/Readme-Logo.png?raw=true)

# HTML5 Speedtest

No Flash, No Java, No Websocket, No Bullshit.

This is a very lightweight Speedtest implemented in Javascript, using XMLHttpRequest and Web Workers.

[official peoject](https://github.com/adolfintel/speedtest/tree/docker)

## Try it
[Take a Speedtest](http://speedtest.fdossena.com)

## Compatibility
Only modern browsers are supported (IE11, latest Edge, latest Chrome, latest Firefox, latest Safari)

## Features
* Download
* Upload
* Ping
* Jitter
* IP Address
* Telemetry (optional)
* Results sharing (optional)

![Screenshot](https://speedtest.fdossena.com/screenshot.png)


## Requirements
 - A reasonably fast web server with PHP (see doc.md for details and use without PHP)
 - Your server must accept large POST requests (up to 20 Megabytes), otherwise the upload test will fail
 - It's also better if your server does not use compression, but it's not mandatory

## Quick installation videos
* [Debian 9.0 with Apache](https://fdossena.com/?p=speedtest/quickstart_deb.frag)
* [Windows Server 2016 with IIS](https://fdossena.com/?p=speedtest/quickstart_win.frag)
* [Ubuntu (External)](https://freedif.org/how-to-install-selfhosted-speedtest)

Also, here's an [example config on Ubuntu 16 LTS](https://github.com/adolfintel/speedtest/issues/50)

## How to use in your site
* See the examples
* [Read the wiki](https://github.com/adolfintel/speedtest/wiki)
* Read doc.md

## Docker + Docker Compose

The project includes a basic `docker-compose.yml` for development.  To run, execute the following:

```
$ docker-compose build

$ docker-compose up
```


Speedtest will be available at [http://0.0.0.0:8888/](http://0.0.0.0:8888/).  You can try out all of the examples via their associated urls (i.e. `http://0.0.0.0:8888/example1.html`).

To run via Docker directly:

```
$ docker build -t vank3f3/speedtest:latest .

$ docker run -d --name  speedtest -p 0.0.0.0:666:80 vank3f3/speedtest:latest
```

## Multiple test servers
Please see the ```mpot``` branch

## Node.js backend
A Node.js implementation is available in the ```node``` branch, maintained by [dunklesToast](https://github.com/dunklesToast).
