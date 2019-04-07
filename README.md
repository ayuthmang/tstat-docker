# Tstat in docker

Tstat in container, see more on [Docker Hub](https://hub.docker.com/r/blacksourcez/tstat/).

## Build docker file to docker image

```bash
docker build 3/ubuntu/
```
## Using Tstat on Container

```bash
$ docker run --name=bs-tstat -v /root/tstat-logs:/root/tstat-logs --rm --net=host -it blacksource/tstat tstat -l -i <your interface name> -s /root/tstat-logs
```

## License

Tstat is provided under the GPL software license and made available for free for personal and research usage. If you plan to use it for commercial usage, [you should go to their homepage](http://tstat.polito.it/software.php). 


## Special Thanks

Thanks for https://hub.docker.com/r/andreyferriyan/tstat/ for make run command fullfilled.
