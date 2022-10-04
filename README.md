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

![image](https://user-images.githubusercontent.com/106013408/193827215-a6c7ed10-a4aa-426f-bf78-f312c460dc05.png)

Das Passwort muss allerdings nach dem ersten Einloggen geändert werden.

### Docker exec

Als nächstes wollen wir auf das Terminal des MySQL Containers zugreifen, damit wir MySQL ausführen können.

```
docker exec -it container_name bash
```

  - `-i` interaktiver Modus, bedeutet, dass der STDIN geöffnet bleibt.
  
  - `-t` allokiert ein pseudo-tty.



  
