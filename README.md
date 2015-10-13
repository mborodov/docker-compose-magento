# Quick deploy developer Magento project

![Screenshot of my docker-compose](http://i.imgur.com/EZ2q3Hb.jpg)

## About 
This container is optimized for running Magento using NGINX and PHP-FPM

## Installation
Clone the repository to your current magento project (after composer update command).

```bash
git clone https://github.com/mborodov/docker-compose-magento.git .
```
*After clonning to project folder, change BASE_URL in docker-compose.yml*

## Import database

Put "dump.sql.gz" to project root folder and execute script:
```bash
docker exec -it kmplzt_web_1 /scripts/import.sh
```
Where kmplzt_web_1 the project cotainer name, for show list of containers in current directory use:
```bash
docker-compose ps
```
## Manage Project
**Attention: Run all command from current project folder**

### Start container

```bash
docker-compose up -d
```
### Stop running containers

```bash
docker-compose stop
```
### XDebug start/stop:

```bash
/scripts/xdebug-start.sh
/scripts/xdebug-stop.sh
```

## Comments
In our example the magento container is linked to the mysql container under the alias **db**.
This means that you'll have to edit your config file in such a way that the mysql host is no longer localhost but db.

*Enjoy!*

