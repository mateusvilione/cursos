# Git e Github

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
Git Alura> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        arquivo1.txt
        arquivo2.txt

nothing added to commit but untracked files present (use "git add" to track)
```
depois do `git add .` 

Git Alura> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   arquivo1.txt
        new file:   arquivo2.txt



-----

lista de comandos |  
---------|----------------------
git add .| adiciona todos os arquivos 


Lista de comando   | Descrição
------------------ | ---------
git add . | Adiciona todos os arquivos ao commit
git add --all | 
git add -A | 
git add ./dir/* | 