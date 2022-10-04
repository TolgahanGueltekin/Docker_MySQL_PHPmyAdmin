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

**docker run** erstellt anhand des Imagenamen einen Container
   
   - `-p` leitet den Standardport auf einen anderen Port um.
   
   - `--name` gibt dem Container einen Namen.
   
   - `-d` der Container läuft im Hintergrund.

### Docker logs

Beim Erstellen eines neuen Containers wird automatisch ein Passwort von MySQL generiert.

Mit dem Befehl `docker logs container_name` kann man das Passwort einsehen.

![image](https://user-images.githubusercontent.com/106013408/193820291-b20f90f3-f65d-44bd-bad2-f15e17e1e958.png)

Das Passwort muss allerdings nach dem ersten Einloggen geändert werden.





  
