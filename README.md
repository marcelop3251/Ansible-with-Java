# Ansible-with-Java

### This application have one sample of how you can started with coded infrastructure.

## Tecnologies

This project uses Ansible, Vagrant and Virtual Box

We going to provisioning two machines, one for our DATABASE and one for our API.

### Getting Started

- Install Ansible 2.9.6.
Details of how to install can be found here. https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
- Install Vagrant
Details of how to install can be found here.
https://www.vagrantup.com/
- Install Virtual Box.
Details of how to install can be found here.
https://www.virtualbox.org/

After of install clone this project at you machine local.

This tutorial was development at machine linux, Ubuntu 18.

At root of your project run the following command.

**vagrant up**

This command will create two machines one for DATABASE and one for API

Now we going to config our machines.

**ansible-playbook -i hosts provisioning.yml**
- It's can be a little time.

At first time that you run this command, you will needed confirm access to virtual machine. Only type **yes**.

First will be install postgres and after that our application made at kotlin.

You can be details about our application [here](https://github.com/marcelop3251/kotlin-exposed-koin-javalin).

Wheter all it is ok, so we can do request for our API.

We going to use curl fo create our first request.

```
curl -X POST \
  http://172.17.177.40:7000/registry-client \
  -H 'Accept: */*' \
  -d '{
  "name": "Marcelo",
  "age": "31",
  "address": {
    "street": "Rua são paulo",
    "city": "Barrinha",
    "number": "1000"
  }
}'
```
Now, going to get all register.

```
curl -X GET   http://172.17.177.40:7000/registry-client   -H 'Accept: */*'
```

I hope you enjoyed :)
