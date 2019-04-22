Example CICD App
=========

A simple python application running in a Docker container.

Getting started
---------------
Download Vagrant for docker containers


## Linux Containers

The Linux stack uses Python, Node.js, .NET Core (or optionally Java), with Redis for messaging and Postgres for storage.

> If you're using [Docker Desktop on Windows](https://store.docker.com/editions/community/docker-ce-desktop-windows), you can run the Linux version by [switching to Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers), or run the Windows containers version.

Run in this directory:
```
python app\generator.py
```

Tests:
```
python -m pytest -v tests/test.py
```

Run flask app in this directory:
```
python app\api.py
```
The app will be running at [http://localhost:5000](http://localhost:5000)

Dockerize the app:
```
docker build -t cicd .
```

Run the Dockerized app:
```
docker run -p 5000:5000 cicd
```


Note: Enable Jenkins + MS Teams connector so that the notiifications will be sent to Teams Channel
