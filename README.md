#GEN : Laboratoire 1

##Membre du groupe : Jeremy Zerbib

###Repo git : https://github.com/jerozerbib/GEN_Labo1
###Commandes effectuées : 


``` bash
# clonage du repo (avec le commit initial uniquement)
git clone git@github.com:jerozerbib/GEN_labo1.git
cd GEN_labo1

# Premier commit sur la branche master
echo "# GEN_Labo1" >> README.md
git add README.md
git add firstC.txt
git commit -m "second commit"
git push

#Creation de la branche essai
git branch essai
git checkout essai

#Premier commit sur la branche essai
touch 1stCessai1
git add 1stCessai1
git commit -m "first commit on branch essai"
git push --set-upstream origin essai

#Deuxième commit sur la branche essai
touch 2ndCessai1
git add 2ndCessai1
git commit -m "second commit on branch essai"
git push --set-upstream origin essai

#Troisieme commit sur la branche essai
touch 3rdCessai1
git add 3rdCessai1
git commit -m "third commit on branch essai"
git push --set-upstream origin essai

#Deuxieme commit sur la branche master
git checkout master
touch master
git add master
git commit -m "third commit on master"
git push

#Merge entre les branches master et essai sur le deuxième commit
git checkout essai
git log                     #Sert à voir le hash du commit voulu
git checkout master
git merge a6abf39aa3b64918fb98623e6366b93b65b17e9b
git push

#4ème commit sur la branche essai
git checkout essai
git touch 4thCessai1
touch 4thCessai1
git add 4thCessai1
git commit -m "fourth commit on essai"
git push --set-upstream origin essai

#Création d'une nouvelle branche qui sera supprimée plus tard
git checkout master
git branch toBeDeleted

#Premier commit sur la branche toBeDeleted
git checkout toBeDeleted
touch 1stCtoBeDeleted
git add 1stCtoBeDeleted
git commit -m "first commit on branch toBeDeleted"
git push --set-upstream origin toBeDeleted

#Merge de la branche essai sur la branche master
git checkout master
git merge essai
git push

#Retour sur le deuxième commit et création de la branche dev
#Hash de la branche est le même que celui retrouvé précédemment
git checkout a6abf39aa3b64918fb98623e6366b93b65b17e9b
git branch dev

#Premier commit sur la branche dev
git checkout dev
touch 1stCdev
git add 1stCdev
git commit -m "first commit on branch dev"
git push --set-upstream origin dev

#Création de la branche essai3
git branch essai3
git checkout essai3

#Premier commit sur la branche essai3
touch 1stCessai3
git add 1stCessai3
git commit -m "first commit on branch essai3"
git push --set-upstream origin essai3

#Suppression de la branche toBeDeleted
git checkout master
git merge toBeDeleted
git push
git branch -D toBeDeleted
git push --delete origin toBeDeleted

```
