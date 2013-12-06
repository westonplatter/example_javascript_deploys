example_javascript_deploys
==========================

Examples for provision servers and deploying Javascript (nodejs/meteor) apps


__1. Setup Vagrant__
```sh
vagrant up
```

__2. Setup the deploy folders__
```sh
ansible-playbook\
  simpleapp-setup.yml\
  -i hosts\
  -u vagrant\
  -c ssh\
  --private-key=~/.vagrant.d/insecure_private_key
```

__3. Deploy the app__
```sh
ansible-playbook\
  simpleapp-deploy.yml\
  -i hosts\
  -u vagrant\
  -c ssh\
  --private-key=~/.vagrant.d/insecure_private_key
```
