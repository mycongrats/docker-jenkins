#### PULL镜像
docker pull mycongrats/jenkins
#### 启动容器
docker run --name jenkins \\  
-p 80:8080 \\  
-v /your/jenkins/lib:/var/lib/jenkins \\  
-dt mycongrats/jenkins
#### 登录容器
docker exec -ti jenkins bash
#### 退出容器
exit
#### 浏览器访问
http://[your ip address]:80
#### 查看初始化密码
cat /your/jenkins/lib/secrets/initialAdminPassword  
或  
docker logs --tail 30 jenkins  
或  
docker exec jenkins cat /var/lib/jenkins/secrets/initialAdminPassword  

