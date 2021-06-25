This project is/will be a indirectly connected project of [SneakAttack](https://github.com/ReplyAttack/)

![](/img/ReplayAttack-Banner-DF.png)

## TO DO

- [ ] Develop `build.sh` that will build all of the tools
- [ ] Develop `latest.sh` that will pull the latest version for each tool
- [ ] Develop `Makefile` that will do the following
   - [ ] Builds all the dockerfiles in the repository.
   - [ ] Checks all the latest versions of the Dockerfile contents.
   - [ ] Run a Dockerfile from the command at the top of the file
   - [ ] Build a Dockerfile
   - [ ] Runs the tests on the repository.
   - [ ] Tests the changes to the Dockerfiles build.
   - [ ] Runs the shellcheck tests on the scripts.


# Install Dockerfile

```
cd cybersecurity-dockerfiles
bash install-docker.sh
```

## Build and run

You could build a specific tool by using the ```docker build``` command:

```
docker build {path_to_dockerfile} -t asonger/{tool_name} --no-cache

```

Each of the Dockerfiles should have a run command at the top of the file, but usually you could just use:

```
docker run -it asonger/{tool_name}
```



