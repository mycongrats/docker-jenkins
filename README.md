#### PULL镜像
docker pull mycongrats/jenkins
#### 启动容器
docker run --name jenkins \\  
-p 80:8080 \\  
-v /mydata/maintenance/lib/docker-jenkins:/var/lib/jenkins \\  
-dt mycongrats/jenkins
#### 登录容器
docker exec -ti jenkins bash
#### 退出容器
exit
#### 浏览器访问
http://[your ip address]:80
#### 初始化密码
docker logs --tail 30 jenkins  
或  
docker exec jenkins cat /var/lib/jenkins/secrets/initialAdminPassword  

