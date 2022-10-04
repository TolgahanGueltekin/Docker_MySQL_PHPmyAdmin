# Docker_MySQL_PHPmyAdmin
Schritt für Schritt Anleitung zur Erstellung eines mysql und phpmyadmin Containers in Docker.

## MySQL Container erstellen und Konfigurieren


### Docker pull

Bevor wir den Container erstellen können, müssen wir zuerst das Image mit folgendem Befehl holen:
  
   `docker pull mysql/mysql-server:latest`

### Docker run
  
   `docker run --name container_name -dp new_port:default_port image_name`
   
   `-p` leitet den Standardport auf einen anderen Port um.
   
   `--name` gibt dem Container einen Namen.
   
   `-d` der Container läuft im Hintergrund.
**3. **
  
