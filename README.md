## v0.1

To Do :
- [ ] Traduire en anglais 

###### `[FR]`
Tuto installation Ansible sur `Rocky Linux 8`

Voici le lien de la documentation Ansible : https://docs.ansible.com/

 

1 Pré-requis ```Ansible ```

  * Mettre à jour la liste de paquets ```sudo dnf update>```
  * Aoivr les paquets git installés ```sudo dnf install git>```
  * Autoriser les répertoires EPEL ```sudo dnf install epel-release```
  * Installer un serveur OpenSSH ```sudo dnf install openssh-server ```
  * Activer le SSH ```systemctl enable ssh```
  * Autoriser le port 22 ```firewall-cmd --zone=public --permanent --add-port=22/tcp```

2 Installation d'```Ansible```

  * Installation des paquets ```sudo dnf install ansible```
  * vérification de la version installée ```ansible --version```
> ansible `<2.9.21>`
config file = /etc/ansible/ansible.cfg

3 Configuration du serveur qui manage Ansible
> Pour installer ou gérer le déploiement sur un serveur cible, il faut créer une pair de clé SSH sur le serveur hébergeant Ansible

  * Créer la pair de clé ```ssh-keygen```
  * Copier la clé générée sur le serveur cible ```ssh-copy-id user@adresseIP```

Ansible est désormais installé et utilisable

  4 Test de connexion entre le serveur Ansible et le serveur cible
  > 2 méthodes sont possibles
   * Ping ``` ping adresseIp```
   * Connexion SSH ```ssh user@adresseIp``` 
