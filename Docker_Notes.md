1.docker是基于go语言开发的。

2.镜像、容器和仓库

```
镜像（Image）：好比是一个模板，可以通过这个模板来创建容器服务，通过一个镜像可以创建多个容器（最终服务运行或者项目运行就是在容器中的）。
容器（container）：独立运行一个或者一个组应用。基本命令：启动、停止、删除等。可以把容器理解为一个简易的linux系统。
仓库（repository）：仓库是存放镜像的地方。仓库分为公有仓库和私有仓库。
```

3.docker为什么比VM快？

> docker不需要像虚拟机一样重新加载一个操作系统内核，避免引导。虚拟机是加载Guest OS，分钟级别的，而docker是利用宿主机的操作系统，省略了这个复杂的过程，秒级。

4.docker rmi：删除镜像

5.有了镜像才可以创建容器

6.docker ps：列出当前正在运行的容器

docker ps -a：列出当前正在运行的容器+历史运行过的容器

7.docker run：创建并运行容器

8.退出容器

```shell
exit #直接容器停止并退出
Ctrl+P+Q  #容器不停止退出
```

9.删除容器

```shell
docker rm 容器id        #删除指定的容器，不能删除正在运行的容器，如果要强制删除 rm-f
docker rm -f $(docker ps -aq)  #删除所有的容器
docker ps -a -q|xargs docker rm   #删除所有的容器
```

10.启动和停止容器的操作

```shell
docker start 容器id    # 启动容器
docker restart 容器id  # 重启容器
docker stop 容器id     # 停止当前正在运行的容器
docker kill 容器id     # 强制停止当前容器
```



