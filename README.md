# reproducer-doctrine-messenger

Install the symfony binary first.

```bash
git clone git@github.com:OskarStark/reproducer-doctrine-messenger.git && \
    cd reproducer-doctrine-messenger && \
    symfony composer install && \
    docker-compose up -d && \
    symfony console doctrine:database:drop --if-exists --force && \    
    symfony console doctrine:database:create && \
    symfony console make:migration
```

I get the following error, because I don't have any entity right now:
```
[error] Error thrown while running command "make:migration". Message: "No mapping information to process"


In NoMappingFound.php line 13:

  No mapping information to process


make:migration [-h|--help] [-q|--quiet] [-v|vv|vvv|--verbose] [-V|--version] [--ansi] [--no-ansi] [-n|--no-interaction] [-e|--env ENV] [--no-debug] [--] <command>

exit status 1
```
