# PicVid - Docker

PicVid kann auch als Docker Stack eingerichtet werden.

### Installation

Das PHP-Image muss vor der Einrichtung des Docker Stack erstellt / aktualisiert werden:  
`docker build -t php-picvid ./php-picvid`

Der Docker Stack mit den verschiedenen Services wird mit dem folgenden Befehl erstellt:  
`docker stack deploy -c docker-compose.yml picvid`