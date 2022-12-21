# mial2001_infra
mial2001 Infra repository
# Исследовать способ подключения к someinternalhost в одну команду из вашего рабочего устройства
ssh -i ~/.ssh/mial2001alekseev -J mial2001alekseev@158.160.53.148 mial2001alekseev@10.128.0.29
<<<<<<< HEAD
#для подключения по имени, нужно создать файл .ssh/config с содержимым:

cat <<EOF> config

=======
# для подключения по имени, нужно создать файл .ssh/config с содержимым:
>>>>>>> 4997570580d6959cf2c70f1d111f8d219ff24317
## bastion
host bastion
user appuser
hostname 158.160.53.148
IdentityFile ~/.ssh/appuser

## someinternalhost
host someinternalhost
user appuser
hostname 10.128.0.29
proxyjump bastion
<<<<<<< HEAD
     
=======
>>>>>>> 4997570580d6959cf2c70f1d111f8d219ff24317
