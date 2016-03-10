# symfony in docker


# start & config docker machine

```
docker-machine start default

eval $(docker-machine env default)
```

# copy docker-compose.yml & other folders/files to symfony-project dir:

```
.
├── ReadMe.md
├── code
│   └── Dockerfile
├── config
│   ├── nginx
│   │   ├── nginx.conf
│   │   ├── php54.conf
│   │   ├── php56.conf
│   │   └── php70.conf
│   ├── php54
│   │   ├── php-fpm.conf
│   │   └── symfony.ini
│   ├── php56
│   │   ├── php-fpm.conf
│   │   └── symfony.ini
│   └── php70
│       ├── php-fpm.conf
│       └── symfony.ini
├── docker-compose.yml
├── php54
│   └── Dockerfile
├── php56
│   └── Dockerfile
├── php70
│   └── Dockerfile
└── symfony-project
    ├── LICENSE
    ├── README.md
    ├── app
    ├── bin
    ├── composer.json
    ├── composer.lock
    ├── src
    ├── vendor
    └── web
```

# build

```
docker-compose build
```

# deploy

```
docker-compose up -d
```

# command 

```
alias sf='docker-compose run php ./app/console'
```



