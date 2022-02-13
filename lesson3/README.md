Если на тестовых нодах возникнет ошибка:
"Failed to download packages: No URLs in mirrorlist"
Необходимо в командной строке ноды применить следующие команды:

sudo sed -i -e "s|mirrorlist=|#mirrorlist=|g" /etc/yum.repos.d/CentOS-*
sudo sed -i -e "s|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g" /etc/yum.repos.d/CentOS-*

