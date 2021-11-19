## v0.1

To Do :
- [ ] Traduire en anglais

###### `[FR]`
Tuto installation d un DNS sur `Rocky Linux 8` via Ansible
Le package

1 Pre-requis ```Ansible ```

Avoir les paquets suivants installes :

  * ```openssh-server```
  * ```git```

On peut enfin commencer
  * Autoriser les repertoires EPEL ```sudo dnf install epel-release```
  * Update la liste de paquets ```sudo dnf update>```
  * Activer le SSH ```systemctl enable sshd```
  * Autoriser le port 22 ```firewall-cmd --zone=public --permanent --add-port=22/tcp```

2 Installation d'```Ansible```

  * Installation des paquets ```sudo dnf install ansible```
  * vérification de la version installée ```ansible --version```
> ansible `<2.9.21>`
config file = /etc/ansible/ansible.cfg

Ansible est désormais installé et utilisable

  3 Test de connexion entre le serveur Ansible et le serveur cible
  > 2 méthodes sont possibles
   * Ping ``` ping adresseIp```
   * Connexion SSH ```ssh user@adresseIp```
