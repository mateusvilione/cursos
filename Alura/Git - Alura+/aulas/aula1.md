# [Episódio 01: Como o git funciona?](https://docs.google.com/presentation/d/15sDU0Angc3erQWtdSPOgxbl2mjQ6tAJigOaydL06pb8/edit#slide=id.g479b3e53c1_0_250)

Fluxo comum

```
git add .
git commit -m "Mensagem do commit"
git pull
git push
```

**git add .**:

**git commit -m "MSG"**: conjunto de alterações que são fechadas em um pacote de alterações com uma mensagem atrelado a essa alteração.

diretorio de trabalho é igual a Working directory

rodando o comando `git status` irá aparecer no console que estamos na `On branch master`, que não temos commits `No commits yet`, o `untracked files` são os arquivos não relacionados ao commit, são recem criados ou modificados, e o git sugere para usar o `git add <files>` para adicionar ao pacote (commit).

```
> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   arquivo1.md
        new file:   arquivo2.md

nothing added to commit but untracked files present (use "git add" to track)
```

depois do `git add .` 

```
> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   arquivo1.md
        new file:   arquivo2.md
```

Como o git funciona?

`tree .git`

```
> tree .git
Listagem de caminhos de pasta
O número de série do volume é FCE7-B37D
C:\REPOSITORY\GIT - ALURA+\.GIT
├───hooks
├───info
├───objects     --> São os arquivos criados (Blobs)
│   ├───83
│   ├───be
│   ├───info
│   └───pack
└───refs
    ├───heads
    └───tags
```

Hash feita em Sha1 para identificar o commit `3c8dce6`

```
> git commit -m "Primeiro commit"
[master (root-commit) 3c8dce6] Primeiro commit
 2 files changed, 1 insertion(+)
 create mode 100644 arquivo1.md
 create mode 100644 arquivo2.md
```

Histórico do repositório

```
> git log
commit 3c8dce685fd75b1c72ffc161d17eaccca357da2b (HEAD -> master)
Author: Mateus Vilione <mateusvilione@gmail.com>
Date:   Tue Mar 17 17:54:42 2020 -0300

    Primeiro commit
```

Ver o fluxo do git `gitk --all` 

-----

|Lista de comando       | Descrição                           |
|-----------------------|-------------------------------------|
|git add .              | Adiciona todos os arquivos ao commit|
|git add --all          |                                     |
|git add -A             |                                     |
|git add ./dir/*        |                                     |
|git rm -- cached <file>| Remove os arquivos do pacote        |