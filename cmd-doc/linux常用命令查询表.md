### Linux常用命令查询表

#### 安装
`rpm -qa | grep <name>` #查看是否安装了某个包<br/>
`yum install <name>` #安装某个包<br/>

#### 打包和解压
`tar -xzvf name.tar.gz` #解压name.tar.gz<br/>
`unzip -xzvf name.zip` #解压name.zip<br/>
`tar -d name.tar.gz name` #压缩并打包name目录，为name.tar.gz<br/>
`zip -r resin.zip resin-3.1.2` #压缩并打包

#### 远程登录
`ssh publish@10.10.100.10 -p16333` #远程登录机器<br/>
`scp -r <folder> -P 16333 publish@10.10.100.10:/data/` #scp上传某个目录<br/>
`rz -y` #上传某个文件<br/>
`sz <filename>` #下载某个文件<br/>

#### 网络

#### 权限
`chown -R www:www /data/tomcat` #给某个目录赋用户和组<br/>
`chmod -R g+x /data/tomcat` #给某个目录赋执行权限<br/>

#### shell
`awk -F '-' '{print $2}'` #按照“-”字符切分字符串，并取第二个字符串<br/>

#### 服务器支持
`ln -s /usr/local/resin-3.1.2 /usr/local/resin` #软连接<br/>
`find -type f -name '*.php'|xargs grep 'GroupRecord'` #查找某个字符串出现在哪个文件中<br/>
`du -h --max-depth=1 work/testing/*` #某个目录下的空间大小分布<br/>

#### 随机密码
`date +%s | sha256sum | base64 | head -c 16 ; echo` <br/>
`date +%s | md5sum | base64 | head -c 10 ; echo`<br/>
`date +%s | md5 | base64 | head -c 32 ; echo`<br/>
`openssl rand -base64 16`<br/>