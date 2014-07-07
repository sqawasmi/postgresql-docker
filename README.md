Docker build for Postgresql 9.3
================================

This repository provides Dockerfile for Postgresql 9.3 with SSH access, initally created to be used by but not limited to `shaker/odoo` docker image.

Started from: http://docs.docker.io/examples/postgresql_service/

### Status
Ubuntu: 14.04
Postgresql: 9.3

Built images are uploaded to [index.docker.io][1]

### Usage:

 - Install Docker: [http://docs.docker.io/][2]
 - Execute
 `docker run -d --name postgresql shaker/postgresql`
 - to run with SSH on port `2222`
 `docker run -d --name postgresql -p 2222:22 shaker/postgresql`
 - If you like to expose postgresql port too:
 `docker run -d --name postgresql -p 2222:22 -p 5432:5432 shaker/postgresql`
 - Stop and start again
   - `docker stop postgresql`
   - `docker start postgresql`
 - ssh `root` password is `postgresql` - you should change it if you exposed ssh port.
 - directories that can be mounted by docker (to allow backup of config, logs and databases):
   - configuration: `/etc/postgresql`
   - logs: `/var/log/postgresql`
   - db data: `/var/lib/postgresql`

  [1]: https://index.docker.io/u/shaker/
  [2]: http://docs.docker.io/en/latest/ "docs.docker.io"
