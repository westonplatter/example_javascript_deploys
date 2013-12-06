example_javascript_deploys
==========================

Examples for provision servers and deploying Javascript (nodejs/meteor) apps


__Setup Vagrant__
```sh
vagrant up
```

__Setup the deploy folders__
```sh
ansible-playbook simpleapp-setup.yml -i hosts -u vagrant
```

Sometimes throws an error (would love to learn why). To mitigate that issue, I 
add the connection type and the private key.
```sh
ansible-playbook\
  simpleapp-setup.yml\
  -i hosts\
  -u vagrant\
  -c ssh\
  --private-key=~/.vagrant.d/insecure_private_key
```

__Deploy the app__
```sh
ansible-playbook -i hosts -u vagrant simpleapp-deploy.yml
```
