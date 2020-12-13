# Timezone application deployment

## Roles
The playbook has 3 roles:
1. **docker**: Installs docker from the stable repository (download.docker.com)
1. **nginx-proxy**: Starts [nginx-proxy](https://github.com/nginx-proxy/nginx-proxy) and [letsencrypt-nginx-proxy-companion](https://github.com/nginx-proxy/docker-letsencrypt-nginx-proxy-companion) containers 
1. **tzapp**: Start [timezone app](https://github.com/14MR/timezone-app) in docker with specified host from `playbook.yml`

## How to use

For local run with Vagrant:

```
   vagrant up
   ansible-playbook -i inventory --limit local playbook.yml
```

For remote:
1. Put your destination server into inventory file / in the command below specify your own path
1. `ansible-playbook -i inventory --limit remote playbook.yml`

