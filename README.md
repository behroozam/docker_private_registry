# Docker Private registry
when i was looking for a easy way to setup a registry server i cant find anything useful . so its easy and minimal setup.
### installation 
create ssl valid certification with letsencrypt or any valid certificate and linked in ssl and certs directory. names must be `fullchain.pem` and `privekey.pem`. 
in next step change your domain in `docker-compose.yml`
and in final `docker-compose up -d` to run server .
for creating user password  use `docker run --entrypoint htpasswd registry:2 -Bbn "user" "password"` and put in in `auth_config.yml`