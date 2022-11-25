
	CONTENT          MODULES
	
	POST_READ(获取http头部初始值)          realip
	SERVER_REWRITE                        rewrite
	FIND_CONFIG(在nginx中间层做location匹配)
	REWRITE                               rewrite
	POST_REWRITE
	PREACCESS                             limt_conn limit_req