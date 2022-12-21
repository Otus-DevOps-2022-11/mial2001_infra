# mial2001_infra
mial2001 Infra repository
# Исследовать способ подключения к someinternalhost в одну команду из вашего рабочего устройства
ssh -i ~/.ssh/appuser -J appuser@51.250.2.165 appuser@10.128.0.4
# для подключения по имени, нужно создать файл .ssh/config с содержимым:
## bastion
host bastion
user appuser
hostname 51.250.2.165
IdentityFile ~/.ssh/appuser

## someinternalhost
host someinternalhost
user appuser
hostname 10.128.0.4
proxyjump bastion
