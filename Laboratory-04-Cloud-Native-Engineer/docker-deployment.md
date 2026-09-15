# Checkpoint 5: Container Lifecycle

1. `docker ps`
   * Lists all active, currently running containers on the system.

2. `docker stop my-nginx`
   * Gracefully stops the running NGINX container.

3. `docker ps -a`
   * Lists all containers, including stopped ones, to verify that the NGINX container has exited.

4. `docker rm my-nginx`
   * Permanently removes the stopped NGINX container from the host system.
