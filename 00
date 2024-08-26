sudo apt install -y git
git config -l
git config --global user.email "email@dominio.com"
git config -l
ssh-keygen -t rsa -b 4096 -C "youremail@example.com"

cat /home/alumno/.ssh/id_rsa.pub
Copiar la llave en:
Perfil >> Setting >> SSH and GPG  Keys >> SSH keys >> New SSH Key
Agregar la llave copiada

sudo vi /home/alumno/.ssh/config
# Agregar:
Host *
  AddKeysToAgent yes
  #UseKeychain yes // Sólo para mac
  IdentityFile ~/.ssh/id_rsa

Agregando la llave
eval $(ssh-agent -s)
ssh-add /home/alumno/.ssh/id_rsa

cd /var/www/html/laravel/app01/
git init .
git add .
git remote add origin git@github.com:gdiazes/laravel.git
git remote -v
git remote set-url origin git@github.com:gdiazes/laravelapp.git
git push origin main
