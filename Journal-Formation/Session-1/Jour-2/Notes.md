# Notes

## Session 1

### Jour 2

#### Compétences

Si on lis les docs en vue de transmettre, on capte 80% du contenu
Alors que transmise, on ne récupère que 20%
=> toujours être actif sur la récupération des informations.

#### Mode concentré

#### Mode diffus

Plus on est loin de la solution, plus il faut se détacher pour créer le lien.

* Y aller par étape
* Répéter les apprentissages pour que cela rentre
* Lire,
  * Pratiquer,
    * Si pas compris, relire
    * Expliquer

* Lire, se rappeler tout les jours, si pas de rappel, relire

#### GIT

Vérifier :

* Modifier fichier.txt
* git add fichier.txt
* Modifier fichier.txt
* git add fichier.txt
* git reset HEAD fichier.

Quels version de fichier est récupérée (celle après le 1er add ? celle d'origine ?)

Revoir le fonctionnement de la commande git merge

#### Linux

## Etape 1 : Le minimum vital

* *Testez la première commande pour vous repérer dans le terminal avec `pwd`.
  * *Retour du répertoire courant
* *Affichez le contenu du dossier dans lequel vous vous trouvez.

  ```shell
  ls
  ls -l pour afficher une liste (droit, date, nom, ...)
  ls -a pour afficher les fichiers cachés
  ```

* *Créez un dossier `linux` qui contiendra les fichiers et dossiers pour l'exercice.

  ```shell
  mkdir linux
  ```

* *Créez un fichier `notes.txt`.

  ```shell
  touch notes.txt
  ```

* *Affichez le contenu du fichier `notes.txt`.

  ```shell
  cat notes.txt
  more notes.txt
  ```

* *Utilisez un éditeur de texte embarqué dans la console comme `nano` pour écrire dans le fichier.
  
  ```shell
  nano notes.txt
  ```
  
  Editer le fichier

* *Sauvegardez le fichier.
  
  Faire *Ctrl+O* pour sauvegarder ces modifications

  Faire *Ctrl+X* pour quitter Nano
* *Affichez à nouveau le contenu du fichier.

```shell
  cat notes.txt
  more notes.txt
  ```

* *Faites un nouveau dossier `sauvegardes`.

```shell
  mkdir -p /home/sylvain/linux/sauvegardes
  ```
  
  le -p permet de créer tout les répertoires inexistants du chemin

* *Copiez le fichier `notes.txt` dans le dossier `sauvegardes` et renommez le en `notes-sauvegarde.txt`.
  
  ```shell
  cp notes.txt /home/sylvain/linux/sauvegardes/.
  mv /home/sylvain/linux/sauvegardes/notes.txt /home/sylvain/linux/sauvegardes/notes-sauvegarde.txt
  ```

* *Affichez le contenu du dossier sauvegarde.

## Etape 2 : Pour aller plus loin

* *Trouvez l'adresse IP de votre machine.

```shell
ifconfig
ip -
```

* *Trouvez le numéro de processus du terminal `bash` que vous avez ouvert.

```shell
ps -ef | grep bash
```

* *Ouvrez un logiciel en utilisant le bureau et tuez le processus avec votre terminal.

```shell
kill -9 <PID_logiciel>
```

* *Donnez le temps moyen qu'un paquet informatique passe sur le serveur entre votre terminal et un serveur de France TV.

```shell
ping www.france.tv
```

* *Donnez le nombre de routeurs qu'il y a entre vous et les serveurs de France TV.

```shell
traceroute www.france.tv
tracepath www.france.tv
```

* *Ecrivez un script `bash` qui prend en paramètre une chaine de caractère pour ensuite afficher le message : _Bonjour cher **entrée**_.
Créer un fichier afficher_msg.sh et ajouter ces lignes 

```shell
#!/bin/bash
echo Bonjour cher $1
```

Changer les droits du fichiers pour le rendre executable

```shell
chmod 744 afficher_msg.sh
```

Executer votre script

```shell
./afficher_msg.sh Moi
```

* *Ecrivez un script `bash` qui vous demande votre nom pour ensuite afficher le message : _Bonjour cher **entrée**_.

* *Utilisez un `cron` pour créer un nouveau fichier vide toutes les 5 minutes qui sera nommé comme suit : _dd-MM-yyyy-HH-mm.log_.

Créer un fichier creer_file.txt

```shell
#!/bin/bash
namefile=`date +"%d-%m-%Y-%H-%M.log"`
touch ~/linux/$namefile
```

Editer la crontab et ajouter 

```shell
*/5 * * * * /home/sylvain/linux/creer_file.sh >/dev/null 2>&1
```

## Étape 3 : Vers l'∞ et au delà !

* *Décompresser [l'archive contenant le site web banksy en 1993](../ressource/banksy.zip) dans un répertoire.

* *Compter combien il y a de fichiers d'extension`.jpg` sous l'arborescence `www.banksy.co.uk`.
* *S'il y a un fichier d'extension `.jpg` qui n'est **pas** une image, le trouver.
