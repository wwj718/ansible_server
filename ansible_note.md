#查看机器信息
ansible   test -m setup

#查看连接情况
ansible   all -m ping

#跑脚本
ansible-playbook server_startup.yml

#tags:只跑一个task
ansible-playbook server_startup.yml --tags "z"
