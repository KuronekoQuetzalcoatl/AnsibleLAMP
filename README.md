LAMP en Ubuntu 
Este playook instala un server LAMP  (Linux, Apache, MySQL and PHP) en Ubuntu

1.- Configuraciones principales
---
mysql_root_password: the password for the MySQL root account.
app_user: a remote non-root user on the Ansible host that will own the application files.
http_host: your domain name.
http_conf: the name of the configuration file that will be created within Apache.
http_port: HTTP port, default is 80.
disable_default: whether or not to disable the default Apache website. When set to true, your new virtualhost should be used as default website. Default is true.


2.- Configuracion delos Defaults default.yml
---
mysql_root_password: "mysql_root_password"
app_user: "sammy"
http_host: "your_domain"
http_conf: "your_domain.conf"
http_port: "80"
disable_default: true


3.- Comado para la ejecucion del playbook 
---
ansible-playbook --inventory inventory/hosts lamp_server.yml
