# <div align=center>my-project</div>
## папка ansible
## клонировать репозиторий
```bash
git clone https://github.com/rasulovdd/my-project.git
```
## создать свой конфиг и отредактировать
```bash
cd my-project
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
## из папки my-project, создаем пользователя
```bash
ansible-playbook playbooks/create-user.yml
```
## пример:
```info
Введите имя пользователя для создания: test03
Введите SSH-ключ для пользователя: ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCpIuThPBVi4FtVVF
Добавить sudo права? (y/n, по умолчанию n) [n]: y
Введите пароль для пользователя:
confirm Введите пароль для пользователя:
```
<br/>

# <div align=center>playbook remove-user</div>
## из папки my-project, удаляем пользователя
```bash
ansible-playbook playbooks/remove-user.yml
```
## пример:
```info
Введите имя пользователя для удаления:: test01
Удалить домашнюю директорию? (yes/no): [no]: yes
```