# Author -> Sachin Gupta <ersachin2602@gmail.com>
Magento 2.4 Installtion using docker
PHP Version 7.4
Mysql Version 8
Elastic Search 7.9.0
Adminer

## Installation

```bash
Step 1 -> Clone this Repostiory on your machine
Step 2 -> Create the new folder inside docker-magento2.4 folder -> src
Step 3 -> go inside the docker-magento2.4 folder and open in the terminal
Step 4 -> RUN Command -> ./bin build ->  it will pull the required images and will setup the Magento Required Enviorment
Step 5 -> RUn Command -> ./bin run ->  it will make your system update
Step 6 -> download the magento 2.4 and place it under src folder as root directory
Step 7 -> run the below command to install the magento
```
```bash
php -d memoery_limit=6G bin/magento setup:install --base-url=http://localhost:8092/ \
--db-host=db --db-name=magento2 \
--db-user=anaya_mage --db-password=anaya_pass \
--admin-firstname=Magento --admin-lastname=User --admin-email=user@example.com \
--admin-user=admin --admin-password=admin123 --language=en_US \
--currency=USD --timezone=America/Chicago --cleanup-database \
--sales-order-increment-prefix="ORD$" --session-save=db --use-rewrites=1 \
--search-engine=elasticsearch7 --elasticsearch-host=es01 \
--elasticsearch-port=9200
```

## Note
```bash
You can change your db password, user and database as per your requirement by changing the configuration in docker-compose.yml
```

## Permission
```bash
Give write permission to es01 and es02 folder.
```

## Run Command on local machine
```bash
sysctl -w vm.max_map_count=262144
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
