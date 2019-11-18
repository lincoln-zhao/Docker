> 阿里云docker仓库
> https://cr.console.aliyun.com/cn-hangzhou/instances/repositories  
> 参考手册
> https://cr.console.aliyun.com/repository/cn-hangzhou/dreamit/image-repo/details

``` 
(1)登录到阿里云docker仓库
sudo docker login --username=itcrazy2016@163.com registry.cnhangzhou.aliyuncs.com
(2)输入密码
(3)创建命名空间，比如itcrazy2016
(4)给image打tag
sudo docker tag [ImageId] registry.cn-hangzhou.aliyuncs.com/itcrazy2016/testdocker-image:v1.0
(5)推送镜像到docker阿里云仓库
sudo docker push registry.cn-hangzhou.aliyuncs.com/itcrazy2016/test-dockerimage:v1.0
(6)别人下载，并且运行
docker pull registry.cn-hangzhou.aliyuncs.com/itcrazy2016/test-dockerimage:v1.0
docker run -d --name user01 -p 6661:8080 registry.cnhangzhou.aliyuncs.com/itcrazy2016/test-docker-image:v1.0
