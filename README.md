# git-challenge

Member 4 -------------------------------------
🧠 Astuces Git à connaître absolument
1. git stash – Sauvegarder temporairement les changements
📌 Utile pour changer de branche sans valider le travail en cours.

git stash         # Sauvegarde les fichiers modifiés
git stash list    # Affiche la liste des stashes
git stash apply   # Restaure le dernier stash (sans le supprimer)
git stash pop     # Restaure et supprime le dernier stash
git stash drop    # Supprime un stash spécifique

2. git revert – Annuler proprement un commit
📌 Crée un nouveau commit qui annule les effets d’un commit précédent.

git revert <commit_hash>
✅ Utilisé en environnement partagé (collaboratif) pour éviter de réécrire l’historique.

3. git reset – Revenir à un état antérieur
⚠️ Risque de perte de données en local (ne pas utiliser après push sans coordination).

git reset --soft <commit>    # Garde les fichiers dans le staging
git reset --mixed <commit>   # Garde les fichiers dans le workspace (par défaut)
git reset --hard <commit>    # Supprime tous les changements

4. git log – Visualiser l’historique des commits

git log --oneline --graph --all --decorate
📊 Affichage compact et visuel de l’historique de toutes les branches.

5. git cherry-pick – Appliquer un commit spécifique ailleurs

git cherry-pick <commit_hash>
🔀 Utile pour copier un correctif ou une fonctionnalité d’une branche vers une autre.

6. git diff – Voir les différences entre deux états

git diff                # Changements non encore indexés
git diff --staged       # Changements déjà indexés
git diff <commit1> <commit2>

7. git clean – Supprimer les fichiers non suivis

git clean -f        # Supprime les fichiers
git clean -fd       # Supprime fichiers + dossiers
🧹 Nettoyage rapide du dossier de travail (⚠️ irréversible).

8. git reflog – Retrouver des commits perdus

git reflog
🧭 Historique des HEADs. Très utile après un reset ou un rebase mal maîtrisé.