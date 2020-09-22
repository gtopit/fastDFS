## 本文档针对centos7下的fastDFS文件系统的安装
### 0、需要安装 yum install -y gcc-c++
### 1、官网下载需要的版本（https://github.com/happyfish100/fastdfs.git ）
### 2、解压，进入解压目录，参考INSTALL安装文件步骤进行安装
### 3、修改/etc/fdfs/tracker.conf、/etc/fdfs/storage.conf配置文件
### 4、fastDFS提供了nginx扩展模块的形式访问存储的文件，因此下载扩展模块（https://github.com/happyfish100/fastdfs-nginx-module ）
### 5、参考INSTALL安装
### 6、编译安装nginx，官网下载需要的版本（https://github.com/nginx/nginx ）
### 7、下载nginx所需依赖
#### yum install -y pcre-devel zlib-devel openssl-devel 
### 8、生成Makefile文件
#### 进入nginx解压目录，执行./auto/configure --add-module=/home/yuqing/fastdfs-nginx-module/src ，然后执行make && make install
### 9、注意将fastDFS nginx扩展模块的mod_fastdfs.conf配置文件拷贝到/etc/fdfs/下，并修改mod_fastdfs.conf。
### 10、启动nginx, /usr/local/nginx/sbin/nginx，查看/usr/local/nginx/logs下有没有错误日志，有则相应的排除。
