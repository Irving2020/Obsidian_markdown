
	CONTENT          MODULES
	
	POST_READ(获取http头部初始值)          realip
	SERVER_REWRITE                        rewrite
	FIND_CONFIG(在nginx中间层做location匹配)
	REWRITE                               rewrite
	POST_REWRITE
	PREACCESS(预检连接数/每秒请求数)        limt_conn limit_req
	ACCESS(校验账户/请求)          auth_basic,access,aut_request
	POSTACCESS
	PRECONTENT                            try_files
	CONTENT                               index,autoindex,concat
	LOG                                   access_log