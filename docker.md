# Docker

## 概念

* ### [镜像(Image)][imageUrl]

1. #### 获取镜像

      * **获取**  
      从Docker镜像仓库获取镜像的命令是`docker pull`，其命令格式为：

        ```docker
        docker pull [选项] [Docker Registry 地址[:端口号]/]仓库号[:标签]
        ```

        具体的选项可以通过`docker pull --help`命令看到  
        * Docker镜像仓库地址：地址的格式一般是<域名/IP>[：端口号]。默认地址是Docker Hub
        * 仓库名：如之前所说，这里的仓库名是两段式名称，即<用户名>/<软件名>。对于Docker Hub，如果不给出用户名，则默认为library，也就是官方镜像。

      * **运行**  
      `docker run`就是运行容器的命，下面是一个简单的例子

         ```docker
          docker run -it --rm ubuntu:18.04 bash
          ```

        * `-it`：这是两个参数，一个是 -i：交互式操作，一个是 -t 终端。我们这里打算进入 bash 执行一些命令并查看返回结果，因此我们需要交互式终端。
        * `--rm`：这个参数是说容器退出后随之将其删除。默认情况下，为了排障需求，退出的容器并不会立即删除，除非手动 docker rm。我们这里只是随便执行个命令，看看结果，不需要排障和保留结果，因此使用 --rm 可以避免浪费空间。
        * `ubuntu:18.04`：这是指用 ubuntu:18.04 镜像为基础来启动容器。
        * `bash`：放在镜像名后的是 命令，这里我们希望有个交互式 Shell，因此用的是 bash。

2. #### 列出镜像

3. #### 删除本地镜像

* ### [容器(Container)][containerUrl]

* ### [仓库(Repository)][RepositoryUrl]

[imageUrl]:https://yeasy.gitbook.io/docker_practice/basic_concept/image
[containerUrl]:https://yeasy.gitbook.io/docker_practice/basic_concept/container
[RepositoryUrl]:https://yeasy.gitbook.io/docker_practice/basic_concept/repository
