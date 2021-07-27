# Todo :

This service is written in NodeJS, Hence need to install NodeJS in the system.


To Update and Install nodejs run below commands :

```
# apt update
# apt install npm -y
# useradd -m -s /bin/bash todoapp
# cd /home/todoapp/
```
Lets clone the code from github repository.

```
# git clone https://github.com/zelar-soft-todoapp/todo.git
# cd todo/
# npm install
```


Finally start the Todo Module once to effect the changes by the below cammand.

```
# mv /home/todoapp/todo/systemd.service /etc/systemd/system/todo.service
# systemctl daemon-reload && systemctl start todo && systemctl enable todo 
```
;) :) ;'( :'( ;)
# RELEASE 0.0.6 -DATE - 03-06-2021
# RELEASE 0.0.6 -DATE - 09-06-2021
