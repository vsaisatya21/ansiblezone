# Goal: Deploy any java based web application into tomcat server

## How??
### 1. Install suitable java version
### 2. Set Java Environment varisbles
### 3. Install tomcat with specific version
### 4. Copy the java application (.war) into <tomcatdirectory>/webapps/<app.war>


## where or which Operarting systems needed to be supported
### Ubuntu 16 and Centos 7

##1
1.sudo apt-get update
2.sudo apt-get install tomcat7
3.curl http://qt.in/test.war -o /var/lib/tomcat7/webapps/test.war

##2
tasks:
- apt:
    name: tomacta7
    update_cache: yes
    state: present
- get_url:
    url: http://qt.in/test.war
    dest: /var/lib/tomcat7/webapps/test.war
handler:
- name: restart tomcat
  service: 
    name: tomcat7
    state: restarted  



