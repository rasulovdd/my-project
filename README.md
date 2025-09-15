# <div align=center>my-project</div>
## папка ansible
## клонировать репозиторий
```bash
git clone https://github.com/rasulovdd/my-project.git && cd my-project
```
## создать свой конфиг и отредактировать
```bash
cp ansible.cfg.sample ansible.cfg
nano ansible.cfg
```

## структура папки
```info
my-project/
├── inventory/   # файлы инвентаризации
├── playbooks/   # основные плейбуки
├── roles/       # роли
├── group_vars/  # переменные для групп хостов
├── host_vars/   # переменные для отдельных хостов
├── files/       # дополнительные файлы
├── ansible.cfg  # конфиг файл
└── ansible.log  # лог файл
```
---
<br/>

# <div align=center>playbook create-user</div>
## пример создание пользователя на всех серверах группе [ubuntu] которые указаны в /inventory/hosts:
в файл /inventory/hosts добавляем свои сервера 
```info
#пример ubuntu серверов
[ubuntu]
test1 ansible_host=192.168.1.10
test2 ansible_host=192.168.1.11
```
# запускаем команду из папки my-project
```bash
ansible-playbook playbooks/create-user.yml -l ubuntu
```
## вот как это выглядит:
```info
Введите имя пользователя для создания: test03
Введите SSH-ключ для пользователя: ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCpIuThPBVi4FtVVF
Добавить sudo права? (y/n, по умолчанию n) [n]: y
Введите пароль для пользователя:
confirm Введите пароль для пользователя:
```

-----
<br/>

# <div align=center>playbook remove-user</div>
## пример удаления пользователя со всех серверов группы [ubuntu] которые указаны в /inventory/hosts
```bash  
ansible-playbook playbooks/remove-user.yml -l ubuntu
```
## вот как это выглядит:
```info
Введите имя пользователя для удаления:: test01
Удалить домашнюю директорию? (yes/no): [no]: yes
```

