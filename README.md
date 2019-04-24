## Benjamin Giralt - TP B3 Ansible

Ce tp **ANSIBLE** a été réalisé et testé sous **Vagrant**  avec deux machines sous **Centos 7** :
* web (192.168.200.201)
* mysql (192.168.200.202)

Dans le répertoire du dépôt (où se trouve le *Vagrantfile*, démarrer les machines virtuelles avec vagrant (en utilisant libvirt)
```
vagrant up
```

Lancer le playbook
```
ansible-playbook -i inventory.ini site.yml
```

Tester le bon fonctionnement
```
http://192.168.200.201/wordpress
```

Si besoin de se connecter en ssh aux vms, ajouter la insecure key de vagrant au trousseau ssh
```
ssh-add ~/.vagrant.d/insecure_private_key
```

Se connecter aux machines
```
vagrant ssh web
```

```
vagrant ssh mysql
```