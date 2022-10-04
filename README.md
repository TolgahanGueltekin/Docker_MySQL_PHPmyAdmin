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
   
   - `-p` leitet default_port(Standardport) auf new_port um.
   
   - `--name` gibt dem Container den Namen container_name.
   
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

### Mysql starten

Da wir uns jetzt im Bash des MySQL Containers befinden, können wir MySQL starten.

```
mysql -uroot -p
```

  - `-uroot` spezifiziert den root als user
  - `-p` ???

![image](https://user-images.githubusercontent.com/106013408/193835800-22c2ad58-9188-4f18-9819-6e66328bb4d3.png)

Der Nutzer wird aufgefordert das generierte Passwort einzugeben. 

Wenn die Anmeldung erfolgreich verlaufen ist, müssen wir nur noch das Passwort ändern.

Mit

```
ALTER USER 'root'@'localhost' IDENTIFIED BY 'newpassword';
```
legen wir ***newpassword*** als neues Passwort fest.


## MyPhpAdmin Container erstellen

### Docker pull

Zuerst das phpmyadmin Image holen

```
docker pull phpmyadmin:latest
```

### Docker run

Wir erstellen anhand des Images einen phpmyadmin Container

```
docker run --name container_name -dp new_port:default_port --link mysql_container_name:db phpmyadmin
```
  - `--link` verbindet den phpmyadmin Container mit mysql_container_name.
  




  
