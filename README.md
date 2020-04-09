# Ansible: Multiple applications with Traefik 2.x and Docker

This is an [Ansible](https://www.ansible.com) playbook to install multiple applications on a single Ubuntu server with [Docker](https://www.docker.com) and [Traefik 2.x](https://traefik.io) updated with [Watchtower](https://github.com/v2tec/watchtower).

## Requirements

+ Ansible >= 2.5

## Tools

This playbook is designed to install a bunch of useful tools:

+ Curl
+ Docker
+ fail2ban
+ Git
+ htop
+ ntp
+ tmux
+ Traefik 2.x
+ Vim
+ ZSH + Oh My Zsh with "ys" theme + zsh-autosuggestions plugin

## Installing on production

Copy the hosts example file and change the values to your needs:

```bash
$ cp hosts.example.ini hosts.ini
```

Setup your variables in the `playbook.yml` file.

Then run the playbook:

```bash
$ ansible-playbook -i hosts.ini playbook.yml
```

## Contributing

There is still a lot of work to do !

Do not hesitate to contribute to the project by adapting or adding features ! Bug reports or pull requests are welcome.

## License

This project is released under the [MIT](http://opensource.org/licenses/MIT) license.
