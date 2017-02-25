# Run MODX in Docker container

Materials for lesson about how to run MODX on Docker environment

Hot to setup environment?

## Preparation

Install Docker and Docker Compose tools. More infromation here https://www.docker.com/products/overview

## Run containers

For run all containers just run command:

```
docker-composer up -d
```

For stop and remove all containers run command:

```
docker-compose down
```

## Install MODX

You can use Gitify (already installed in docker image) for installing MODX. Just log into container with MODX (php in services) and run gitify command.

```
docker exec -it foldername_php_1 bash
../../Gitify/Gitify modx:install

```

**NOTE!** foldername - name of folder where you store this code. Docker always creates containers names by this rule: current folder name + service name + number of instance.

Or you can download MODX file into src folder and setup MODX by usual MODX installer.

## Open instance in browser

By default this configuration use port 3333 for website, so you should go to ` http://0.0.0.0:3333` but you can change it in docker-composer.yml and restart all containers.
