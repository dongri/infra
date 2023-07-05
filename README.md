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
