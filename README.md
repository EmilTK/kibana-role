Kibana-role
=========

Данная роль предназначена для установки Kibana в учебных целях.

Requirements
------------

  * Ansible > 2.9
  * Elasticsearch instance

Role Variables
--------------

  variable | Description | Default
 --- | --- | ---
 kibana_version | Устанавливаемая версия Kibana | 7.14.0
 kibana_install_type | Тип установки | remove
 elastic_instance | Адрес инстанса Elasticsearch | IPv4 хоста `el-instance` при наличии такого в инвентари, в случае его отсутствия - `0.0.0.0`


Example Playbook
----------------

``` yml
- name: Install kibana
  hosts: kibana
  roles:
    - kibana
```

License
-------

MIT

Author Information
------------------

Emil Temerbulatov - студент курса DevOps Netology