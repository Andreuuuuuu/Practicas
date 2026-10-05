# Instal·lació d'un servidor LEMP

**Implantació d'Aplicacions Web**
**2 ASIX**
Andreu Company Delfa

Instalamos mariadib

*Figura 1: server*
> Es veu `sudo apt install mariadb-server`. Demana contrasenya, falla una autenticació i després mostra que ja està en la versió més recent.

Ejecutamos la configuración segura

*Figura 2: secure*
> Es veu `mariadb-secure-installation` i un missatge indicant que MariaDB és segura per defecte en Debian i que aquest script és innecessari.

Creamos la base de datos

*Figura 3: Base de Datos 1*
> Es veu `mysql -u root -p`, s'introdueix la contrasenya i s'accedeix al monitor de MariaDB. Es crea la base de dades `newdb` amb `CREATE DATABASE newdb;`.

*Figura 4: Base de Datos 2*
> Es veu la creació de l'usuari `andreu`@`10.0.2.15` amb `CREATE USER`, l'assignació de privilegis amb `GRANT ALL PRIVILEGES`, `FLUSH PRIVILEGES` i `quit`.

*Figura 5: php*
> Es veu `apt install nginx php php-fpm php-mysql` i la llista de paquets que s'instal·laran.

*Figura 6: nginx*
> Es veu el navegador mostrant la pàgina "Welcome to nginx!" a l'adreça `http://10.0.2.15`.

*Figura 7: default*
> Es veu l'editor de text mostrant el fitxer de configuració `/etc/nginx/sites-available/default` amb la configuració de `server_name`, `location /` i `location ~ \.php$`.

---
