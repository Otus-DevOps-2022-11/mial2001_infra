# mial2001_infra
mial2001 Infra repository
bastion_IP = 51.250.2.165 
someinternalhost_IP = 10.128.0.4 
#файл .ssh/config для подключения по имени:
#bastion
Host bastion
User appuser
Hostname 51.250.2.165
IdentityFile ~/.ssh/appuser
Host 10.128.0.*
ProxyJump appuser@51.250.2.165
#someinternalhost
Host someinternalhost
User appuser
IdentityFile ~/.ssh/appuser
Hostname 10.128.0.4
ProxyJump appuser@51.250.2.165
