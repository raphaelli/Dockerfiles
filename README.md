# Dockerfiles
Dockerfiles backup and open sources - //自用Dockerfiles轮子

# Dockerfile list
- Mysql by Docker-Compose - [mysql](./mysql)
- PHP&Nginx by Docker-Copmpose - [php_Nginx](./php_Nginx)
- MSSql by Docker-Compose - [mssql](./mssql)
- Gogs by Docker-Compose - [gogs](./gogs)

# Docker 
Remove the old version and install the new one.

```
$ sudo apt-get remove docker docker-engine docker.io
$ curl -fsSL get.docker.com -o get-docker.sh
$ sudo sh get-docker.sh
$ #Or  curl -sSL https://get.docker.com/ | sh 
```



# Docker Compose

- Get docker compose

  ```sh
  $ sudo curl -L "https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
  
  ```

- Apply executable permissions to the binary

  ```sh
  $ sudo chmod +x /usr/local/bin/docker-compose
  ```

- Test the installation.

  ```sh
  $ docker-compose --version
  docker-compose version 1.22.0, build 1719ceb
  ```


# Automatically start

## Ubuntu
```
$ vim  /etc/rc.local
## add
/usr/local/bin/docker-compose -f /docker/mssql/docker-compose.yml up -d
```

>Using  `docker logs` check something you want in logs.