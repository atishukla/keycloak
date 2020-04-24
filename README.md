### Setup local instance of keycloak

- This will be separate from kubernetes apiserver
- This can be LDAP in the organisation
- This requires https
- In order for this to work with DNS level certs we need to communicate with public ip
- We achieve this from local docker machine by adapting the hosts file something like 127.0.0.1 keycloak.xxx.learn-xx.xyz
- Edit the docker-compose.yaml to include the token or keys for domain provider
- create blank acme.json to hold certificates, ensure the permission is 0600 touch acme.json && chmod 0600 acme.json