
# DevOps lab_roles

## Описание

`lab_roles` — это учебный проект, демонстрирующий использование Ansible для автоматизации настройки веб-сервера Nginx. Проект включает в себя инвентарный файл, плейбук, роль Ansible и скрипт для запуска.

## Структура проекта

```bash
lab_roles/
├── inventory.ini        # Инвентарный файл с определением хостов
├── playbook.yml         # Основной Ansible-плейбук
├── roles/
│   └── nginx-vhosts/    # Роль Ansible для настройки виртуальных хостов Nginx
└── run_playbook.sh      # Скрипт для запуска плейбука
```

## Предварительные требования

* Установленный [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
* Доступ по SSH к целевым хостам
* Python на целевых хостах

## Установка

1. Клонируйте репозиторий:

   ```bash
   git clone https://github.com/L453R1337/lab_roles.git
   cd lab_roles
   ```

2. Убедитесь, что файл `inventory.ini` содержит актуальные данные о ваших хостах.

## Использование

Для запуска плейбука выполните:

```bash
./run_playbook.sh
```

Скрипт `run_playbook.sh` запускает Ansible-плейбук `playbook.yml` с использованием инвентарного файла `inventory.ini`.

## Структура роли `nginx-vhosts`

Роль `nginx-vhosts` предназначена для настройки виртуальных хостов Nginx. Она включает в себя задачи по установке Nginx, настройке конфигурационных файлов и перезапуску службы.
