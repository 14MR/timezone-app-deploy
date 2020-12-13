# Timezone application deployment

## Functionality and structure
The playbook does have 2 roles:
1. Install docker from the stable repository (download.docker.com)
1. Start [timezone app](https://github.com/14MR/timezone-app) on port 80 in docker

## How to use

For local run with Vagrant:

```
   vagrant up
   ansible-playbook -i inventory --limit local playbook.yml
```

For remote:
1. Put your destination server into inventory file / in the command below specify your own path
1. `ansible-playbook -i inventory --limit remote playbook.yml`

