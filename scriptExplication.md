# Voici la documentation qui explique le fonctionement de mon code

1. Le playbook Ansible est nommé "Automatiser la configuration d'Apache2" et s'exécute sur tous les hôtes spécifiés.

2. La directive `become: yes` permet d'exécuter les tâches avec les privilèges d'administration.

3. La première tâche installe Apache2 en utilisant le module `apt`, qui garantit que le package "apache2" est présent sur les hôtes cibles.

4. La deuxième tâche copie le fichier "domains" vers le répertoire "/tmp/domains" sur les hôtes cibles à l'aide du module `copy`. il est bon de savoir que le fichier "domains" doit être dans le même répertoire que le playbook Ansible.

5. La troisième tâche lit le contenu du fichier "domains" en utilisant la commande `cat` à l'aide du module `shell`. Le résultat est enregistré dans la variable `names_output` pour une utilisation ultérieure.

6. La quatrième tâche utilise le module `template` pour créer des fichiers de configuration pour chaque nom de domaine extrait du fichier "domains". Le fichier source utilisé est "site.conf", et les fichiers de configuration générés sont placés dans le répertoire "/etc/apache2/sites-available/" avec une extension ".conf".

7. La cinquième tâche crée des répertoires pour chaque nom de domaine en utilisant le module `file`. Les répertoires sont créés dans le chemin "/var/www/{{ item }}", où `item` représente chaque nom de domaine extrait précédemment.

8. La sixième tâche utilise le module `template` pour créer des pages HTML pour chaque nom de domaine. Le fichier source utilisé est "template.html", et les pages HTML générées sont placées dans le répertoire "/var/www/{{ item }}/index.html", où `item` représente chaque nom de domaine extrait précédemment.

9. La septième tâche active les configurations Apache2 correspondantes en utilisant la commande `a2ensite` avec le nom de fichier de configuration de chaque nom de domaine extrait précédemment.

10. La huitième tâche redémarre le service Apache2 en utilisant le module `service` pour appliquer les modifications de configuration.
