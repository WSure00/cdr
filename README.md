# cdr
> Helps developers move efficiently in the repo directory

> 工具核心思路是使用repo list 和 grep 等组合命令，查找并进入相关项目路径。可以在repo任意目录中使用。

## 使用方法:  
> Ubuntu16.04 为例
### 1、给予执行权限: 
    chmod a+x cdr
### 2、安装: 
    ./cdr -i  
**注: 安装之后请执行 [source ~/.bashrc](url)**
### 3、条件与查找: 
例:
#### &emsp;     i.单条件查找
    cdr preloader (直接进入preloader目录)
#### &emsp;     ii.多条件查找 (空格为区分，后跟目录名称)
    cdr vendor google (会进入vendor/google)
### 4、条件反向查找
例:

    cdr cust proprietary ~trust (会进入同时包含cust proprietary 但是不包含trust的路径)

注: "~" 反向匹配符号，在zsh和bash表现不同，可自行在代码中更改"REVERSE"变量
### 5、进入项目根目录(.repo所在目录)
    cdr 或者 cdr ~

### 6、脚本更新
    cdr -u
### 7、查看使用说明
    cdr -h
## 更新日志
### 1.2
&emsp;i.  增加关键字颜色显示  
&emsp;ii. 增加更新功能
### 1.1
提升速度，修复BUG
### 1.0
初始脚本，提供基础目录跳转功能
