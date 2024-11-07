PENDING TASK DURING VIDEO 

ON ANSIBLE CONTROLLER 

CD /ETC/ANSIBLE
NANO ANSIBLE.CONF --> PASTE UNDER [defaults] -- > It looks like this

gathering = smart
fact_caching_timeout = 86400
fact_caching = redis
fact_caching_prefix = ansible_DevSecOps_Saikiran
fact_caching_connection = PASTE-YOUR-CLIENT(TESTSERVER01)-PUBLICIP-HERE:6379:0

![image](https://github.com/user-attachments/assets/5a3e46dd-2534-4b97-8fff-0a380c747433)

CTLR+X --> Y > ENTER

apt update
apt install -y python3-pip
pip3 install redis

ON CONTROLLER --> ANSIBLE -I INVFILE PVT -M SETUP

ON CLIENT(TESTSERVER01) --> REDIS-CLI --> KEYS *


