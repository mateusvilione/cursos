# Episódio 02: Como o merge funciona?

## Merge

Name                    
  arquivo1. arquivo2. index.js

```
> git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   index.js
```

Cria uma branch

```
> git checkout -b feature

or 

> git branch feature
```

Mostra as branchs

```
> tree .git/refs
Listagem de caminhos de pasta
O número de série do volume é FCE7-B37D
C:\REPOSITORY\GIT - ALURA+\.GIT\REFS
├───heads
└───tags
```

Troca de branch

```
> git switch feature
```

Merge 

junta os arquivos

```
> git merge feature
Updating 3c8dce6..d36a259
Fast-forward --> está apontando pra o commit mais novo
 index.js | Bin 0 -> 6 bytes
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.js
```

Tenta representar a estutura do fluxo do git

```
> git log --decorate --oneline --graph --all
* d36a259 (HEAD -> master, feature) feature
* 3c8dce6 Primeiro commit
```