<h1 align="center">Мониторинг сигнализации Starline</h1>
<p clear="both">
<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="http://fraso777.ru/data/Ztar-Line-logo.png">
  <img alt="ZtarLine" src="http://fraso777.ru/data/Ztar-Line-logo.png" width="600">
</picture>
<p align="center">
  <img src="https://img.shields.io/badge/PHP-7.2.5 or later-blue" />
  <img src="https://img.shields.io/badge/Ubuntu_Server-18.04 or later-blue" />
  <img src="https://img.shields.io/badge/Zabbix-6.0 +-blue" />
  <img src="https://img.shields.io/badge/Apache-1.3.12 or later-blue" />
  <img src="https://img.shields.io/badge/Mysql-8.0.X-blue" />
</p>
</div>

*<h3 align="center">Скрипт ZstarLine нужен для интеграции автомобильной сигнализации Starline в систему мониторинга Zabbix как для личного использования, так и для коммерческого.</h3>*
*<h4 align="center">Данный скрипт тестируется на OC Ubuntu Server 22.04.2 LTS, PHP 8.1.2, Apache 2.4.52, MySQL 8.0.32</h4>*</br></br></br></br></br>




+ [Системные требования](#Системные-требования) 
+ [Установка](#Установка) 
+ [Настройка](#Настройка) 

</br></br></br>


# Системные требования
Данный скрипт работает на установленной системе мониторинга Zabbix начиная с 6 версии и выше. С требованиями к системе вы можете ознакомиться в официальной инструкции -><a href="https://www.zabbix.com/documentation/6.0/ru/manual/installation/requirements" target="_blank">Требования</a>
</br></br></br>

# Установка
<sub>Данное руководство для ubuntu ОС</sub>

Скачиваем скрипт в домашнюю директорию ubuntu
```
sudo git clone https://github.com/Fraso777/ZtarLine.git
```
переходим в скаченную директорию
```
cd ZtarLine/
```
копируем файлы в директорию `/externalscripts` Zabbix[^?]
```
sudo cp ztarline.php user_data.php /usr/lib/zabbix/externalscripts
```
копируем дополнение с картами
```
sudo cp map_ztarline.php /usr/share/zabbix
```
меняем права доступа к файлам, измением владельца и группу
```
sudo chmod 755 /usr/lib/zabbix/externalscripts/ztarline.php
sudo chown root:root /usr/lib/zabbix/externalscripts/ztarline.php
sudo chmod 755 /usr/lib/zabbix/externalscripts/user_data.php
sudo chown root:root /usr/lib/zabbix/externalscripts/user_data.php
sudo chmod 755 /usr/share/zabbix/map_ztarline.php
sudo chown root:root /usr/share/zabbix/map_ztarline.php
```

# Настройка
Переходим на страницу Zabbix 





[^?]: My reference.
