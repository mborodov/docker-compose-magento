# Quick deploy developer Magento project

![Screenshot of my docker-compose](http://i.imgur.com/EZ2q3Hb.jpg)

## Installation

Clone the repository to your current magento project (after composer update command).

```bash
git clone https://github.com/mborodov/docker-compose-magento.git .
```

After clonning to project folder, change BASE_URL in docker-compose.yml

## Manage Project

*Attention: Run all command from current project folder*

### Start container

```bash
docker-compose up -d
```
### Stop running containers

```bash
docker-compose stop
```
### Import database to mysql container (exec from current project folder)
1. Download dump.sql.gz from test server and put to root current project folder
2. Exec import database script from web container

```bash
docker exec -it WEB_CONTAINER_NAME /scripts/import.sh
```

*Enjoy!*

