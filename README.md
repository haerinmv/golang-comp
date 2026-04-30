# golang-comp


Repo perso pour bosser des problèmes de programmation compétitive en Go, surtout dans un format Codeforces.

L'idée n'est pas d'automatiser la réflexion ou d'écrire les solutions à ma place. Le but est d'avoir une structure propre, simple à relire, et une pipeline qui vérifie que le code reste correct après chaque push.

## Organisation

Chaque problème vit dans son propre dossier. Le nom du dossier commence par l'identifiant du sujet avec un `#`, puis une version lisible du titre.

Exemple :

```text
problems/
  #71A-way-too-long-words/
    main.go
```

Si besoin, un dossier peut aussi contenir des samples :

```text
problems/
  #71A-way-too-long-words/
    main.go
    1.in
    1.out
    2.in
    2.out
```

## Convention

- un dossier par exo
- un `main.go` par solution
- le préfixe `#...` sert à retrouver rapidement le problème
- les fichiers `.in` et `.out` servent aux tests simples quand ils existent

## Pipeline

À terme, la CI doit vérifier automatiquement :

- le formatage Go
- la compilation
- l'exécution sur les samples présents dans chaque dossier

La pipeline doit valider le travail, pas imposer la solution.
