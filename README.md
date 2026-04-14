"#Projet DevOps" 

# 1. Introduction
Ce projet a pour but de mettre en pratique les bases de Git : création de branches, manipulation de fichiers et fusion (merge) de branches avec gestion d'historiques.

# 2. Installation de Git
Pour reproduire cet environnement, vous devez installer Git. 
Voici les commandes pour les systèmes principaux :
- Pour Debian/Ubuntu
-- sudo apt update
-- sudo apt install git
- Pour MacOS (via Homebrew)
-- brew install git
- Pour Windows
- Téléchargez l'installeur sur https://git-scm.com/download/win

# 3. Documentation de référence
Les ressources suivantes ont été consultées pour la réalisation de ce projet :
https://git-scm.com/book/fr/v2
https://docs.github.com/fr/authentication/connecting-to-github-with-ssh
https://docs.github.com/fr/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches

# 4. Tableau des commandes réalisées
git init                      -> Initialise un nouveau dépôt Git localement.
git checkout -b develop       -> Crée la branche "develop" et bascule dessus.
touch file1 file2 file3       -> Crée les trois fichiers initiaux (ou type nul > sur Windows).
git add .                     -> Ajoute toutes les modifications à l'index pour le prochain commit.
git commit -m "msg"           -> Enregistre les modifications dans l'historique local.
git push origin develop       -> Envoie la branche locale vers le serveur distant (GitHub).
git merge develop             -> Fusionne les modifications de develop vers la branche actuelle (main).
ren file1 file1.txt           -> Renomme le fichier file1.
del file3                     -> Supprime le fichier file3.

# 5. Diagramme du workflow (Flow de commit)
Voici une représentation visuelle de la structure des branches utilisée dans ce projet :

main    :  (A) ----------------------- (C)   <-- Fusion (Merge)
             \                       /
develop :     (A) --- (B1) --- (B2) --      <-- Travail sur file1, file2, file3

(A) : Initialisation du projet sur la branche main.
(B1, B2) : Commits successifs sur la branche develop (ajout, renommage, suppression).
(C) : Fusion de l'historique de develop vers main.
