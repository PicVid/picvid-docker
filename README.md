# PicVid - Docker

PicVid kann auch in Docker installiert werden.

### Struktur

Durch eine Docker-Compose-Datei können die Grundlagen für PicVid in Docker installiert werden. Es werden dabei die
folgenden Container installiert und eingerichtet:

**Container:**

 - picvid-nginx
 - picvid-php
 - picvid-mysql 

**Verzeichnisse:**

 - `img-data`: In diesem Verzeichnis befinden sich alle Bilder welche in PicVid hochgeladen wurden.
 - `htdocs`: In diesem Verzeichnis befindet sich PicVid. Die Anwendung kann über dieses Verzeichnis aktualisiert werden.
 
**Hinweis:** Die Verzeichnisse `htdocs` und `img-data` müssen vor Verwendung mit entsprechenden Rechten versehen werden
um die Konfiguration schreiben zu können sowie den Upload von Bildern zu ermöglichen:
 
 `chown www-data htdocs img-data`

### Container - Details

#### picvid-nginx

Der NGINX-Container verwendet das [offizielle NGINX-Image](https://store.docker.com/images/nginx).

#### picvid-php

Der PHP-Container verwendet das [offizielle PHP-Image](https://store.docker.com/images/php). Durch ein Dockerfile werden 
zusätzlich die Erweiterungen `pdo_mysql` und `exif` installiert.

#### picvid-mysql
Der MySQL-Container verwendet das [offizielle MySQL-Image](https://store.docker.com/images/mysql).