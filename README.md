# Подготовка  системы виртуализации Proxmox VE на Debian 12

## Системные требования:
* Debian 12
* Локально установленный Ansible

## Описание переменных:
* inventory/main.yaml - переменная "ansible_host", ей задается ip целевого хоста

## Пример запуска
```ansible-playbook -i inventory/main.yaml run.yaml```

## Описание проекта:

Данный проект является по сути автоматизированным официальным мануалом, взятым с [proxmox.com]("https://pve.proxmox.com/wiki/Install_Proxmox_VE_on_Debian_12_Bookworm" "Официальная инструкция")  
*Так же для удобства добавлен nginx с проксирование со стандартного https порта на 8006.*
В дирректории templates лежит конфиг nginx, который средствами Ansible копируется на хост.