# gitpod-sample-project
gitpod sample project

## Build the image

From the repository root, do:

```
$ docker build -t yassend/ubu-dev-base:latest .gitpod/
```

## Push to repository

The hub.docker.com repositpry is at ``https://hub.docker.com/repository/docker/yassend/ubu-dev-base``.

After building the image, first make sure you autheticate, like:

```
$ docker logout
Removing login credentials for https://index.docker.io/v1/
$ docker login
```

```
Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.
Username: yassend
Password:
WARNING! Your password will be stored unencrypted in /root/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
```

Then push the image:

```
$ docker push yassend/ubu-dev-base:latest
```

## Remember to logout

``/root/.docker/config.json`` indeed has your psswd only encoded but
otherwise unprotected. Doing:

```
$ docker logout
```

removes it from there.


Enjoy! ;)
