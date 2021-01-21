# reproducer-doctrine-messenger

Install the symfony binary first.

```bash
symfony composer install && \
    docker-compose up -d && \
    symfony serve -d && \
    symfony console doctrine:database:create && \
    symfony console make:migration
```
