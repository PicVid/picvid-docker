#PicVid - Docker

Diese Konfiguration ermöglicht die einfache Installation von PicVid in Docker. Es werden dabei die folgenden Container
erstellt:

 - picvid-nginx
 - picvid-php
 - picvid-mysql 

Die Verzeichnisse `img-data` und `htdocs` müssen vor Verwendung noch mit entsprechenden Rechten versehen werden:
`chown www-data htdocs img-data`