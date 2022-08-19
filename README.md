# cdr
Helps developers move efficiently in the repo directory

工具核心思路是使用repo list 和 grep 等组合命令，查找并进入相关项目路径。可以在repo项目目录中任意处使用。

使用方法: (Ubuntu为例)
1、下载后给予执行权限: chmod a+x cdr 
2、安装: ./cdr -i                              (安装之后请执行 source ~/.bashrc)
3、条件与查找: (空格为区分，后跟目录名称)
例:
a、单条件查找
cdr preloader (直接进入preloader目录)
b、多条件查找
cdr vendor google (会进入vendor/google)
4、条件反向查找
例:
cdr cust proprietary ~trust (会进入同时包含cust proprietary 但是不包含trust的路径)
注："~" 反向匹配符号，在zsh和bash表现不同，可自行在代码中更改"REVERSE"变量
5、查看使用说明，cdr -h
