HTTP: 
		  ahtuorization : 权限 401
		  authentication: 登录 403

认证方式:Web常见权限认证

			1、session  (寄存于server端)  —— cookie防盗
					mgrE:采用Nginx分发多台服务器负载均衡,造成多台服务器间session互不共享的问题，需采用特殊手段共享数据(1、配置基于客户端hash的负载均衡方案;2、redies存储session机器共享)
			
			2、Authorization —— TYPE_XXXX 
					(eg:Basic_) -> base64 => userId code
					mgrE:依次向每台服务器访问做认证，存在N台服务器，就需要作用N次认证调用N次数据库访问，数据量过大时数据库存在较大压力(express_basicAuth)
					(eg:Bearer_) 
					Bearer类型后面加上经过对称加密(AES=>(uid,screct_key))token(JWT)
			
			