# gitcheatsheet
Cheat sheet pour git

Rebase quand on pull au lieu de merger
======================================
Histoire de garder les historiques propres quand on pull
```sh
git config --global push.rebase true
```

Créer une branche
=================
Création de la branche:
```sh
git checkout -b nouvelle_branche
```

Si vous voulez poussez cette branche sur un remote par exemple origin:
```sh
git push origin nouvelle_branche
```

Tester qu'une branche merge correctement
========================================
Par exemple pour tester que vous pourrez merger votre_branche avec master
```sh
git checkout master
git merge --no-ff --no-commit votre_branche
```
Si cela se passe bien, git va vous le dire "Automatic merge went well; stopped before committing as requested". 
Il ne reste plus qu'à annuler car on faisait juste un test
```sh
git merge --abort
```
