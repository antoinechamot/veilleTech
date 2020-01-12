# GIT


## Config

- git config --global user.name "Toto toto"
- git config --global user.email "Toto@gmail.com"
- git config --global --list
- git config user.name "clone"


## Initialisation du depot

- git init


## Indexer Modif

- git add <files>
- git reset <files>
- git add --patch

## Visualiser modifications

- git diff <files>
- git diff --cached <files>
- git blame -L 10,+5 <file> 


## Naviguer dans l'historique

- git log -n <nbr_commit>
- git log <nom_branche>
- git show <SHA1>
- git checkout <SHA1>


## Tags
- git tag <nom> -m "message ici"
- git tag --delete <nom>
- git tag
- git push <nom_remote> <nom_tag>
- git push origin --tags


## Depots distant

- git clone <remote> <folder_name>
- git remote -v
- git remote show origin
- git remote add origin <chemin_remote>
- git push -u <nom_remote> <nom_branche>
- git fetch <nom_remote>
- git pull

## Sauvegarde
- git stash save "message ici"
- git stash pop <index_stash>
- git stash list
- git stash show <numero_index>

## Merge
- git merge --abort
- git pull --rebase


## Branches
- git branch <nom_branche>
- git checkout <nom_branche>
- git switch <nom_branche>
- git checkout -b <branch_name>
- git switch -c <branch_name>
- git branch -a
- git cherry-pick <sha1_commit>
- git branch -d <nom_branche_a_suppr>
- git push --delete <nom_branche_a_suppr>

## Merge Branches
- git rebase <nom_branche_sur_laquelle_rebase>
- git merge <nom_branche_a_merger>
- git rebase --continue










