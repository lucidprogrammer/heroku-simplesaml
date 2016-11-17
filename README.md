# Base Image for both SP and IDP with specifics for Heroku

If you want to build manually docker build -t lucidprogrammer/heroku-simplesaml . or your own tag.

Heroku uses $PORT env variable to assign a port. So this image uses ${PORT} in the ports.conf and the virtual host for saml on *.

Also, the process is run by heroku using a dynamically created user, so there is no need to chown to apache user.

You may create IDP and SP by using this as base image and adding the necessary configuration files.

```
FROM lucidprogrammer/heroku-simplesaml
```
