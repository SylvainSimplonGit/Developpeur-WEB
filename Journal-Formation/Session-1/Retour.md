# Qu'ai-je retenu ?
## Session 1 
### Jour 1
#### Algorithmie :
* Résoudre un problème avec un méthode qui utilise des données d'entrées, qui suit des contraintes pour aboutir à un résultat déterminé. 
* cette méthode une fois définie donnera toujours le même résultat en fonction des mêmes données d'entrée.

#### GIT
* **git init** : Initialise le répertoire local pour être versionné par GIT
* **git clone** : Récupére une copie identique au repository distant depuis le serveur distant
* **git add \<object>**: Ajoute le fichier ou le répertoire \<object> à l'index du repository local
* **git commit -m "message"** : commit toutes les modifications du repository local en indiquant le "message"
* **git push** : pousse les commits enregistrés sur le repository distant
* **git pull** : récupère les écarts entre le repository distant et local

#### A retenir
* Qu’est ce qu’un algorithme ?

Il s’agit d’une suite (**finie**) d’opérations élémentaires qui permettent de résoudre un problème. C’est une procédure de calcul qui prend en entrée un ensemble E de valeurs et qui retourne en sortie en ensemble E’ de valeurs.

Un algorithme doit toujours se terminer et fournir un résultat. Un algorithme est dit **correct** si pour chaque ensemble de valeurs **E** en entrée il fournit le même ensemble de résultat **E'** en sortie. Afin de s'assurer qu'un algorithme est correct, on peut le prouver de manière formelle. On utilise parfois certains algorithmes non corrects si l'on sait gérer le taux d'erreur de l'algorithme.

* Les clés pour solutionner un problème :
  * **Toujours avoir un plan** (même si le plan risque d’être modifié, cela permet de définir des étapes intermédiaires et de suivre l’avancement de la résolution)
  * **Reformuler le problème** (toujours la première étape du plan !). Cela permet à minima de s’assurer qu’on a compris le problème et parfois de voir le problème sous un autre angle et de trouver plus facilement une solution
  * **Diviser le problème** (cela permet souvent de le simplifier). Exemple avec le tri de livres par hauteur, il vaut mieux trier 100 livres en découpant 25 par 25 puis rassembler les 4 x 25 triés que de trier les 100 d’un coup.
  * **Commencer par ce que l’on sait faire**
  * **Simplifier le problème** (parfois il est préférable de supprimer des contraintes pour avoir une solution intermédiaire plus simple, même si elle ne couvre pas tout le problème).
  * **Chercher les analogies** (ne veut pas dire copier/coller).
  * **Expérimenter** (ne veut pas dire deviner ou faire “au pif”).
  * **Garder la motivation** (éviter de laisser la frustration vous atteindre). Soyez indulgent avec vous même !

* Git
  * git remote add origin <url_du_repo_distant>

### Jour 2