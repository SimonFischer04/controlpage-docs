# Installation

## Prerequisites

  - [Docker](https://www.docker.com/) (including docker-compose)

## Setting up the project

To get a basic setup up and running use the sample docker-compose file here: [docker-compose.yml](https://gitlab.fischerserver.eu/controlpage/controlpage-releases/-/blob/main/docker-compose.yml)

!!! Info

    Basic samples for deploying it on kubernetes can also be found in the [releases repo](https://gitlab.fischerserver.eu/controlpage/controlpage-releases/-/tree/main/k8s), although this way of deploying is (currently) not updated.

### Manually creating Database

The default compose file exposed Adminer on port 8080. So go to ``http://<ip of docker host>:8080`` and login using the root password configured in the compose file. Then run this SQL script to create everything.

```sql
CREATE USER 'ControlPageUser'@'%' IDENTIFIED BY '6xovUH2QmUZooPTyYrpD9Js8fZRrMBrkqHzs4soRdP'; GRANT ALL PRIVILEGES ON `controlpage`.* TO 'ControlPageUser'@'%';
CREATE DATABASE `controlpage`;
```

Then restart docker compose stack.

!!! Note

    this step will be automated in the future

### Configuring settings

Now open the UI at ``http://<ip of docker host>:8008`` and go to the settings tab. The "Backend Host" needs to be configured to ``http://<ip of docker host>:42000`` (or whatever port configured in compose file). Further information can be found here: [Settings](settings.md).

!!! Warning

    This has to be done on EACH client!

## Advanced Setup (not required!)

For a more advanced setup you could for example set up a [reverse proxy](/advanced/reverse-proxy).
