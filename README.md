# Docker

## How Docker run on MacOS

Docker does NOT run natively on MacOS because the MacOS kernel is NOT compatible.
Docker actually run on a VM (Linux kernel).
You can use `nsenter` (namespace enter) container to access Docker VM on MacOS, using this comand:

```sh
$ docker run -it --privileged --pid=host debian nsenter -t 1 -m -u -n -i sh
```

Reference: [Stackoverflow](https://stackoverflow.com/questions/66669224/how-do-i-access-the-docker-ce-virtual-machine-on-macos-bigsur)

## References

- [Docker official document](https://docs.docker.com/get-started/overview/)
- [Docker Education Resources](https://docs.docker.com/get-started/resources/)
- [Docker github](https://github.com/docker)
