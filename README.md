# My Ansible Playbook

This is my Ansible Playbook to fit with Ubuntu Bionic (18.04 LTS) servers.

## Requirements

+ Ansible >= 2.4.0.0

## Applications

This playbook is designed to install [Docker](https://www.docker.com) and a bunch of useful tools :

+ Docker
+ Docker-compose
+ Vim
+ Git
+ htop
+ ntp
+ Curl

## Installing on production

Setup your servers addresses in the ```hosts``` file, then run the playbook :

```bash
$ ansible-playbook -i hosts playbook.yml
```

### Example of hosts file

```yaml
# hosts

[webservers]
example.com

[webservers:vars]
ansible_python_interpreter=/usr/bin/python3

app_name=
app_env=
app_key=
app_debug=
app_log_level=
app_url=

db_connection=
db_host=
db_database=
db_username=
db_password=

broadcast_driver=
cache_driver=
session_driver=
queue_driver=

redis_host=
redis_password=
redis_port=

mail_driver=
mail_host=
mail_port=
mail_username=
mail_password=
mail_encryption=

pusher_app_id=
pusher_app_key=
pusher_app_secret=
pusher_app_cluster=

github_id=
github_secret=
github_url=

twitter_id=
twitter_secret=
twitter_url=
```

## Installing on virtual machine

You can also test this Playbook on a virtual machine for some tests.

Before starting, you need to install :

+ [Vagrant](https://www.vagrantup.com)
+ [Virtualbox](https://www.virtualbox.org)

Then run :

```bash
$ vagrant up
```

The default IP address is ```192.168.50.4```. You need to setup your ```hosts``` and ```~/.ssh/config``` files to give an SSH access to Ansible into your virtual machine.

You could find more informations in [this article](https://guillaumebriday.fr/utiliser-la-commande-ssh-pour-entrer-dans-une-machine-vagrant) (in French).

## Contributing

There is still a lot of work to do !

Do not hesitate to contribute to the project by adapting or adding features ! Bug reports or pull requests are welcome.

## License

This project is released under the [MIT](http://opensource.org/licenses/MIT) license.
