
## Command List

	1、*docker logs*  <container_name_or_id>


## notes


1、容器是映像中包含的应用程序的1个实例
2、一个Docker容器是在一个单独的虚拟网络中运行的，与我们所在的主机网络不同，所以我们不能简单的连接到postgres服务器，运行在容器网络的端口上5432上，除非我们告诉码头工人一种桥梁<bridge>，在我们的本地主机的网络和容器的网络之间，通过使用-p标志，然后指定主机网络的端口，然后是冒号，然后是容器的相应端口
3、通过*docker exec* 命令访问容器外壳bash，容器中会存在一些CLI命令供我们直接从外壳与对应服务器交互
`
	docker exec -it postgres12 /bin/sh
`
`
	![[Pasted image 20221026094943.png]]
`
	
4、使用cmake提升效率 （Win：MINGW）







