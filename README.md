# reproducer-doctrine-messenger

Install the symfony binary first.

```bash
git clone git@github.com:OskarStark/reproducer-doctrine-messenger.git && \
    cd reproducer-doctrine-messenger && \
    symfony composer install && \
    docker-compose up -d && \
    symfony server:stop && \
    symfony server:start && \
    symfony console doctrine:database:drop --if-exists && \    
    symfony console doctrine:database:create && \
    symfony console make:migration
```
