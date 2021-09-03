# 指令說明

將 docker bin & socket mapping 進 jenkins 容器裡，使 jenkins 可以在容器裡使用 docker 指令
```
docker run -d -v /var/run/docker.sock:/var/run/docker.sock \
-v $(which docker):/usr/bin/docker -v jenkins_home:/var/jenkins_home \ -p 8080:8080 -p 50000:50000 nexus-jenkins
```