#GOTHAM (Gathering of Organization Treating Humble Ad-hoc Map)

##Introduce
BATMAN-adv visualization program

This program used d3.js, websocket with JAVA.

##설치(installation)
java 설치(java installation)
```
$ sudo add-apt-repository ppa:webupd8team/java
$ sudo apt-get update
$ sudo apt-get install oracle-java9-installer
$ sudo apt-get install javacc
```
tomcat 설치 (master는 웹 서버 무조건 설치) 
(tomcat installation (master must install web server))
```
$ sudo apt-get install tomcat8
$ cd GOTHAM(vis)/settingFile
$ cp masterWebServer.war /var/lib/tomcat8/webapps
$ sudo service tomcat8 restart
```


master일 경우 - batman-adv & batctl이 무조건 동작하고 있어야 함
(master - batman-adv & batctl must be running)
```
$ cd GOTHAM(vis)/settingFile/master
# sudo java -jar master.jar
```

slave일 경우 - batman-adv & batctl & master가 무조건 동작하고 있어야 함     
(slvae - batmnad-adv & batctl & master must be running)
```
$ cd GOTHAM(vis)/settingFile/slave
# sudo java -jar slave.jar
```

##실행(Execution)
slave 소스코드를 보면 master ip를 넣어줘야 하는 부분이 있습니다.   
지금은 default로 192.168.0.10로 되어있습니다.   
혹시 수정이 필요하면 변경 후 사용바랍니다.
(There is a part that we have to put master ip in slave source code
 Now, the default setting is 192.168.0.10.
 If you want to change it, you can switch it)

