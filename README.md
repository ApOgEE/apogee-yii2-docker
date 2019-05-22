## ApOgEE Docker Container Setup For Yii2 Development
![apogee](notes/badges/apogee-yii2-docker.svg)

I'll be adding Docker compose file to simplify my task here.

### Steps

After clone, run this commands:

1. Docker Compose
```bash
docker-compose up
```

2. After Container setup completed. Turn the docker down.
```bash
docker-compose down
```

### Initializing Yii2 Project

Using this docker setup, you can either clone a yii2 project into `apogee-phpyii2` directory or initialize a new project using composer commands.

#### Initialize new project using composer
If you already have composer in your system, simply run:
```bash
composer create-project yiisoft/yii2-app-basic apogee-phpyii2
```

Or if you don't install it, you may use `composer` within the `phpweb` container. Make sure you run the container first using `docker-compose up -d`

Enter the container using this command:
```bash
docker exec -it <container name> /bin/bash
```

Then run the composer command from html directory.
```bash
cd /var/www/html
composer create-project yiisoft/yii2-app-basic .
```
