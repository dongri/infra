# What is in
* nginx
* postgres
* mysql
* redis

# docker
```
$ docker network create my_network

$ docker-compose up -d
```

# mysql
```
$ mysql -h 127.0.0.1 -u root -ppassword
MYSQL_URL=mysql://root:password@localhost:3306
```

# postgres
```
POSTGRES_URL=postgresql://postgres:@localhost:5432/postgres
```

# mongo
```
MONGODB_URL=mongodb://localhost:27017
```

## Trouble shooting
### chown: changing ownership of '/var/lib/postgresql/data': Permission denied (on Rancher Desktop)
```
$ vim ~/Library/Application\ Support/rancher-desktop/lima/_config/override.yaml

mountType: 9p
mounts:
  - location: "~"
    9p:
      securityModel: mapped-xattr
      cache: "mmap"
```
