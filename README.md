example_javascript_deploys
==========================

Examples for provision servers and deploying Javascript (nodejs/meteor) apps


Setup
```sh
vagrant up
```

Setup the deploy folders
```sh
ansible-playbook -i hosts -u vagrant simpleapp-setup.yml
```

Deploy the app
```sh
ansible-playbook -i hosts -u vagrant simpleapp-deploy.yml
```
