ubuntu@ip-172-31-33-104:~/custom-nginx$ docker --version 
Docker version 29.0.4, build 3247a5a
ubuntu@ip-172-31-33-104:~/custom-nginx$ sudo systemctl status docker
● docker.service - Docker Application Container Engine
     Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
     Active: active (running) since Wed 2025-11-26 04:01:54 UTC; 30min ago
TriggeredBy: ● docker.socket
       Docs: https://docs.docker.com
   Main PID: 3424 (dockerd)
      Tasks: 21
     Memory: 104.5M
        CPU: 1.557s
     CGroup: /system.slice/docker.service
             ├─3424 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock
             ├─4445 /usr/bin/docker-proxy -proto tcp -host-ip 0.0.0.0 -host-port 80 -container-ip 172.18.0.2 -container-port>
             └─4449 /usr/bin/docker-proxy -proto tcp -host-ip :: -host-port 80 -container-ip 172.18.0.2 -container-port 80 ->

Nov 26 04:01:54 ip-172-31-33-104 dockerd[3424]: time="2025-11-26T04:01:54.840776575Z" level=info msg="Docker daemon" commit=>
Nov 26 04:01:54 ip-172-31-33-104 dockerd[3424]: time="2025-11-26T04:01:54.840892345Z" level=info msg="Initializing buildkit"
Nov 26 04:01:54 ip-172-31-33-104 dockerd[3424]: time="2025-11-26T04:01:54.872101814Z" level=info msg="Completed buildkit ini>
Nov 26 04:01:54 ip-172-31-33-104 dockerd[3424]: time="2025-11-26T04:01:54.886505992Z" level=info msg="Daemon has completed i>
Nov 26 04:01:54 ip-172-31-33-104 dockerd[3424]: time="2025-11-26T04:01:54.886625629Z" level=info msg="API listen on /run/doc>
Nov 26 04:01:54 ip-172-31-33-104 systemd[1]: Started Docker Application Container Engine.
Nov 26 04:06:52 ip-172-31-33-104 dockerd[3424]: time="2025-11-26T04:06:52.884412054Z" level=info msg="detected 127.0.0.53 na>
Nov 26 04:06:53 ip-172-31-33-104 dockerd[3424]: time="2025-11-26T04:06:53.427643658Z" level=info msg="sbJoin: gwep4 ''->'6f1>
Nov 26 04:06:53 ip-172-31-33-104 dockerd[3424]: time="2025-11-26T04:06:53.733903758Z" level=warning msg="forcibly turning on>
Nov 26 04:10:41 ip-172-31-33-104 dockerd[3424]: time="2025-11-26T04:10:41.189613448Z" level=info msg="sbJoin: gwep4 ''->'f5f>



*********************************************************************************************************************************************

ubuntu@ip-172-31-33-104:~/custom-nginx$ sudo docker ps
CONTAINER ID   IMAGE                       COMMAND                  CREATED          STATUS          PORTS                                 NAMES
61549f8fa3bc   manikant/custom-nginx:1.0   "/docker-entrypoint.…"   26 minutes ago   Up 26 minutes   0.0.0.0:80->80/tcp, [::]:80->80/tcp   custom-nginx-web-1



*******************************************************************************************************************************************************

ubuntu@ip-172-31-33-104:~/custom-nginx$ sudo docker compose ps
NAME                 IMAGE                       COMMAND                  SERVICE   CREATED          STATUS          PORTS
custom-nginx-web-1   manikant/custom-nginx:1.0   "/docker-entrypoint.…"   web       28 minutes ago   Up 28 minutes   0.0.0.0:80->80/tcp, [::]:80->80/tcp
 

***************************************************************************************************************************************************************

ubuntu@ip-172-31-33-104:~/custom-nginx$ sudo docker images | grep custom-nginx
WARNING: This output is designed for human readability. For machine-readable output, please use --format.
manikant/custom-nginx:1.0   9ccbd2eda877       79.9MB         22.6MB   U    



********************************************************************************************************************************************************************

ubuntu@ip-172-31-33-104:~/custom-nginx$ sudo docker compose ps
NAME                 IMAGE                       COMMAND                  SERVICE   CREATED              STATUS              PORTS
custom-nginx-web-1   manikant/custom-nginx:1.0   "/docker-entrypoint.…"   web       About a minute ago   Up About a minute   0.0.0.0:80->80/tcp, [::]:80->80/tcp


**************************************************************************************************************************************************************







******************
