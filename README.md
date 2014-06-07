Docker build for Postgresql 9.3
================================

This repository provides Dockerfile for Postgresql 9.3 with SSH access.

Started from: http://docs.docker.io/examples/postgresql_service/

### Status
This build still "work in progress".

Built images are uploaded to [index.docker.io][1]

### Usage:

 - Install Docker: [http://docs.docker.io/][2]
 - Execute
 `docker run -d --name postgresql -p 2222:22 shaker/postgresql`
 - Stop and start again
   - `docker stop postgresql`
   - `docker start postgresql`
 - `root` password is `postgresql`

  [1]: https://index.docker.io/u/shaker/
  [2]: http://docs.docker.io/en/latest/ "docs.docker.io"
  [3]: http://127.0.0.1:8069/
