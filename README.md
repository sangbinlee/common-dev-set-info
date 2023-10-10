# common-dev-set-info project

  개발 환경 세팅 정보 

  * road map - 항목 정리 
  * env files( properties , yml)- [local, dev, prd] - windows, linux(ubuntu, centos, mac) 
  * web server (nginx, apache24) - reverse proxy , 
  * docker, 
  * kubernetes, 
  * redis, 
  * db , 
  * nuxt, 
  * next, 
  * ci(jenkins pipline)
  * etc...




# docker.sock
  * jenkins in docker container
  * 
    [sudo] password for master:
    root@kpismain:/home/master# cd /var/run
    root@kpismain:/var/run# ll
    total 40
    drwxr-xr-x 33 root root   1040 Oct 10 09:26 ./
    drwxr-xr-x 23 root root   4096 Sep 29 23:35 ../
    -rw-------  1 root root      0 Oct  5 21:22 agetty.reload
    drwxr-xr-x  2 root root     80 Oct  6 06:24 blkid/
    drwxr-xr-x  3 root root    300 Oct  5 21:22 cloud-init/
    drwxr-xr-x  2 root root     80 Oct  5 21:22 console-setup/
    drwx--x--x  5 root root    140 Oct  5 21:22 containerd/
    drwxr-xr-x  3 root root     60 Oct  5 21:22 credentials/
    -rw-r--r--  1 root root      4 Oct  5 21:22 crond.pid
    ----------  1 root root      0 Oct  5 21:22 crond.reboot
    drwx------  2 root root     40 Oct  5 21:22 cryptsetup/
    drwxr-xr-x  2 root root     60 Oct  5 21:22 dbus/
    prw-------  1 root root      0 Oct  5 21:22 dmeventd-client|
    prw-------  1 root root      0 Oct  5 21:22 dmeventd-server|
    drwx------  8 root root    180 Oct  5 21:22 docker/
    -rw-r--r--  1 root root      3 Oct  5 21:22 docker.pid
    srw-rw----  1 root docker    0 Oct  5 21:22 docker.sock=



# permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post
    참조 사이트 : https://github.com/occidere/TIL/issues/116
        /var/run/docker.sock 파일의 권한을 666으로 변경하여 그룹 내 다른 사용자도 접근 가능하게 변경
            sudo chmod 666 /var/run/docker.sock


                root@kpismain:/var/run# sudo chmod 666 /var/run/docker.sock
                root@kpismain:/var/run# ll do*
                -rw-r--r-- 1 root root     3 Oct  5 21:22 docker.pid
                srw-rw-rw- 1 root docker   0 Oct  5 21:22 docker.sock=






            
        chown 으로 group ownership 변경
            sudo chown root:docker /var/run/docker.sock

                            
# When using COPY with more than one source file, the destination must be a directory and end with a


