# mial2001_infra
mial2001 Infra repository
# Исследовать способ подключения к someinternalhost в одну команду из вашего рабочего устройства
ssh -i ~/.ssh/mial2001alekseev -J mial2001alekseev@51.250.78.57 mial2001alekseev@10.128.0.17
# для подключения по имени, нужно создать файл .ssh/config с содержимым:
Host 10.128.0.*
    ProxyJump mial2001alekseev@51.250.78.57
Host bastion
     HostName 51.250.78.57
     User mial2001alekseev
     IdentityFile ~/.ssh/mial2001alekseev
Host someinternalhost
    ProxyJump mial2001alekseev@51.250.78.57
     HostName 10.128.0.17
     User mial2001alekseev
     IdentityFile ~/.ssh/mial2001alekseev
