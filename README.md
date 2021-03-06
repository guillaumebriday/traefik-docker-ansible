# Ansible: Multiple applications with Traefik 2.x and Docker

![](https://github.com/guillaumebriday/traefik-docker-ansible/workflows/Lint/badge.svg)

This is an [Ansible](https://www.ansible.com) playbook to install multiple applications on a single Ubuntu server with [Docker](https://www.docker.com) and [Traefik 2.x](https://traefik.io) updated with [Watchtower](https://github.com/v2tec/watchtower).

## Requirements

+ Ansible >= 2.5

## Tools

This playbook is designed to install a bunch of useful tools:

+ [Docker](https://www.docker.com)
+ [Traefik 2.x](https://traefik.io)
+ [Watchtower](https://github.com/containrrr/watchtower)

## Installing on production

Copy the hosts example file and change the values to your needs:

```bash
$ cp hosts.example.ini hosts.ini
```

Setup your variables in the `playbook.yml` file.

Then run the playbook:

```bash
$ ansible-playbook -i hosts.ini playbook.yml

# For one role only
$ ansible-playbook -i hosts.ini playbook.yml --tags "traefik"
```

### Example

I use this playbook to deploy Traefik and Docker in production to host [self-hosted services](https://github.com/guillaumebriday/selfhosted-services).

## Contributing

Do not hesitate to contribute to the project by adapting or adding features ! Bug reports or pull requests are welcome.

## License

This project is released under the [MIT](http://opensource.org/licenses/MIT) license.
