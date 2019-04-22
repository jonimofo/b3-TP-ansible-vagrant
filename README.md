## Benjamin Giralt - TP B3 Ansible

Ce tp a été réalisé avec **vagrant**  et deux machines sous **Ubuntu 18.04**

Démarrer les machines virtuelles sous vagrant
```
vagrant up
```

Lancer le playbook
```
ansible-playbook -i inventory.ini site.yml
```

### TODO (restant à faire/améliorer)
* redirection Apache de / sur /wordpress (je m'y suis cassé les deux 2 jours et je n'ai toujours pas réussi)