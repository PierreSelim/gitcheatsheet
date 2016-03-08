# gitcheatsheet
Cheat sheet pour git

Historique propre (push.rebase)
===============================
Histoire de garder les historiques propres quand on pull
```sh
git config --global push.rebase true
```

Branche mergeable ?
===================
Pour tester que vous pourrez merger votre_branche avec master
```sh
git checkout master
git merge --no-ff --no-commit votre_branche
```
Si cela se passe bien, git va vous le dire "Automatic merge went well; stopped before committing as requested". 
Il ne reste plus qu'à annuler car on faisait juste un test
```sh
git merge --abort
```
