# Ansible

## Ansible c'est quoi?

Ansible est une plateforme open-source de gestion de configuration et d'automatisation des tâches. Elle permet de déployer, configurer et gérer des systèmes informatiques à grande échelle de manière simple et reproductible.

## Les choses à savoir sur Ansible

1. Architecture client-serveur : Ansible suit une architecture client-serveur avec un contrôleur et des nœuds gérés.

2. Inventaire : L'inventaire est un fichier qui répertorie les machines distantes sur lesquelles vous souhaitez exécuter des actions.

3. Playbooks : Les playbooks sont des fichiers YAML qui décrivent les tâches à exécuter sur les nœuds gérés.

4. Modules : Ansible utilise des modules pour effectuer des actions spécifiques sur les nœuds gérés.

5. Tâches : Les tâches sont des actions à effectuer sur les nœuds gérés et sont associées à des modules.

6. Commandes ad-hoc : Ansible permet d'exécuter des commandes ponctuelles sans créer de playbook.

## les choses à faire avant d'utiliser ansible

### Installer Ansible

Avant de pourvoir utilisé Ansible, notre première reflexe c'est de l'installer sur notre linux. <br>

on doit d'abord mettre à jour notre linux et aussi notre package. On doit utiliser les commandes suivantes :

` sudo apt update` <br>
`sudo apt upgrade ` <br>

Maintenant on doit installé ansible pour cela, il suffit de taper la commande suivante:

`sudo apt install ansible`
