# Créer un dépot Git, le lier à un dossier local  

Pour pouvoir "sauvegarder" un dossier local, On doit initialiser Git dedans pour que les changemets soit enregistrés, et y lier un dépot distant en guise de déstination.

## Petit Exemple. Pour ce faire, il faut...

- Aller sur [Github](https://github.com), login, un click sur notre avatar en haut à droite, et aller sur la page de nos dépots.

- Sans surprise, cliquer sur le bouton [Nouveau], donner un nom à "la repo" et à y être cliquer sur l'option "Privé".

Depuis l'onglet `< > Code` copier la ligne:

```bash
git remote add origin https://github.com/username/reponame.git
```
- On peut aller dans le répertoire local et initialiser Git  

```bash
cd /home/username/Documents/calepin
git init  
```
- C'est maintenant que l'on colle la ligne copiée
 
- On peut vérifier les "remotes" liées à un dossier, avec:

```bash
git remote -v
```
- Première sauvegarde   

On ajoute tout (avec add .), on crée 'un colis' en y collan un message qui sera affiché avec, et on envoy (push) en ajoutant la mention --set-upstream sinon il va le demander.

```bash
git add . 
git commit -m "FirstCommit"
git push --set-upstream origin master
```
Et Voilà. Pour les prochaines fois, un 'git push' sur la dernière ligne suffira, puique ça partira d'office sur origin master.

## RTFM

[Docs sur git-scm.com](https://git-scm.com/doc)
[Pareil, mais external links](https://git-scm.com/doc/ext)
