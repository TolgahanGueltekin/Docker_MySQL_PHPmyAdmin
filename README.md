# Docker_MySQL_PHPmyAdmin
Schritt für Schritt Anleitung zur Erstellung eines mysql und phpmyadmin Containers in Docker.

## MySQL Container erstellen

**1. Das MySQL Image holen**
  
   `docker pull mysql/mysql-server:latest`

**2. Mit dem Docker run-Befehl den Container erstellen**
  
   `docker run --name container_name -dp port:default_port image_name`
   
   `-p` leitet den Standardport auf einen anderen Port um.
   
   `--name` gibt dem Container einen Namen.
   
   ``
  
