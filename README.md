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
