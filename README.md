## Getting Started

### Try in Play With Docker

<a href="https://labs.play-with-docker.com/?stack=https://raw.githubusercontent.com/frappe/frappe_docker/develop/tests/pwd.yml">
  <img src="https://raw.githubusercontent.com/play-with-docker/stacks/master/assets/images/button.png" alt="Try in PWD"/>
</a>

Wait for 5 minutes for ERPNext site to be created or check `site-creator` container logs before opening browser on port 80.

### Setting up Pre-requisites

This repository requires Docker, docker-compose and Git to be setup on the instance to be used.

For Docker basics and best practices. Refer Docker [documentation](http://docs.docker.com).

### Cloning the repository and preliminary steps

Clone this repository somewhere in your system:

```sh
git clone https://github.com/frappe/frappe_docker.git
cd frappe_docker
```

Set env variables
```sh
cp env-production .env

```

Launch
```sh
docker-compose --project-name [project-name] up -d 

```

Default site is "site1.localhost", add site to hosts file and open it in browser