# custom-postgresql

The dockerfile in this repo will compile the postgresql source code in `./postgresql`. Copy the file `foo` in the container image and `git clone` a random repo.
And create a postgresql image that can be run with a docker command.

# Important Dockerfile commands

1. `COPY <host_file> <container_file>` copies a file from the host filesystem to the image fs.

2. `RUN <command>` allows you to run bash commands in the image fs.


# Important Docker commands

1. Build with `docker build -t posgresql-chris .`

2. Run with `docker run -Ptid -v /tmp:/tmp posgresql-chris`, the `-v` mounts the host path to the container path. Any file written there will appear in the host filesystem.

3. SSH into container with `docker ps` find container name and run `docker exec -ti <name> bash`

4. Stop container with `docker stop <name>` and delete with `docker rm <name>`
