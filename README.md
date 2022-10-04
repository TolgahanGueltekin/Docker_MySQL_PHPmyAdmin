# Docker_MySQL_PHPmyAdmin
Schritt für Schritt Anleitung zur Erstellung eines mysql und phpmyadmin Containers in Docker.

## MySQL Container erstellen und Konfigurieren


### Docker pull

Bevor wir den Container erstellen können, müssen wir zuerst das Image mit folgendem Befehl holen:
  
```Dockerfile
docker pull mysql/mysql-server:latest
```

### Docker run

Nachdem wir das Image nun geholt haben, können wir jetzt den Container erstellen.

Dazu führen wir den folgenden Befehl aus:

```
docker run --name container_name -dp new_port:default_port image_name
```

**docker run** erstellt anhand des Imagenames einen Container
   
   - `-p` leitet den Standardport auf einen anderen Port um.
   
   - `--name` gibt dem Container einen Namen.
   
   - `-d` der Container läuft im Hintergrund.

### Docker logs


  
