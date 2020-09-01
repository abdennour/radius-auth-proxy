# radius-auth-proxy

Alpine Radius Client and Auth-proxy between Radius Server &amp; app - Easy to configure with Env vars.

# Prerequisites:

- docker


# Getting Started

**pull image** `docker pull abdennour/radius-auth-proxy`

**Run it** `docker run -e <CHECK ENV VARS BELOW> -p 8998:8998 abdennour/radius-auth-proxy`

Now navigate to http://localhost:8998

( or better check **demo** section below)

**Full Example** [abdennour/demo-radius-reverse-proxy](https://github.com/abdennour/demo-radius-reverse-proxy/blob/master/README.md)

# Documentation Env Vars

|   env var       | required? |  default | values  |  description |
|------           |---|---|---|---|
| RADIUS_SERVER_SECRET    | yes  | - |   |   |
| RADIUS_SERVER_HOSTNAME  | yes  | - |   |   |
| PROXY_URL                 | yes  | - |   |   |
|  UI_AUTH_TYPE | no  | basic | basic, form  | auth type is it basic auth using default browser prompt or using login form  |
|  RADIUS_SERVER_PORT | no  | 1812  |  - | radius udp port  |
|  RADIUS_AUTH_TIMEOUT |  no |  60 | -  | in seconds - mapped to AddRadiusAuth directive of apache mod_radius  |
|  RADIUS_AUTH_RETRIES | no  | 3  | -  |  mapped to AddRadiusAuth directive of apache mod_radius |
|  RADIUS_COOKIE_VALID | no  | 20  | -  | in minutes - mapped to AddRadiusCookieValid directive of apache mod_radius  |
|  SESSION_CRYPTO_PASSPHRASE | no  |  any-secret-passphrase |  - |  mapped to SessionCryptoPassphrase directive of apache mod_session_crypto |
| SESSION_MAX_AGE  | no  |  1200 | -  | in seconds - mapped to SessionMaxAge directive of apache mod_session_cookie |
| SESSION_COOKIE_NAME  | no  | session  | -  |  mapped to SessionCookieName directive of apache mod_session_cookie |
| SESSION_COOKIE_ATTRS  |  no | path=/  | -  |  mapped to SessionCookieName directive of apache mod_session_cookie |
|   |   |   |   |   |


> Find Uptodate env vars list [here](https://github.com/abdennour/dockerfiles/blob/master/docker-images/radius-auth-proxy/fry#L5-L19)

# References

This software is shipped as container image :

- **image repo** [abdennour/radius-auth-proxy](https://hub.docker.com/r/abdennour/radius-auth-proxy/tags)

- **image source code** [abdennour/dockerfiles::radius-auth-proxy](https://github.com/abdennour/dockerfiles/tree/master/docker-images/radius-auth-proxy)

- **helm chart** [tn/radius-auth-proxy](https://github.com/kubernetes-tn/charts/tree/master/stable/radius-auth-proxy)

# Demo 

- [abdennour/demo-radius-reverse-proxy](https://github.com/abdennour/demo-radius-reverse-proxy/blob/master/README.md)



# Authors

- Abdennour TOUMI <ceo@kubernetes.tn>

# LICENSE

This software is licensed under [GNU GENERAL PUBLIC LICENSE](LICENSE)








