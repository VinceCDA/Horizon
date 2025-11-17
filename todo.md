# NIVEAU 1 – Bases : add, commit, .gitignore

## 1.1. Première sauvegarde
- Vérifier l’état du projet.
- Ajouter tous les fichiers du projet.
- Créer la première sauvegarde avec le message "Initialisation du site Banque Horizon".

## 1.2. Créer le fichier TODO à ignorer
- Créer un fichier `TODO.md` à la racine et y mettre vos notes.
- Vérifier qu’il est bien détecté comme fichier non suivi.
- Créer un fichier `.gitignore` contenant :
  - `TODO.md`
- Vérifier qu’il n’apparaît plus dans les fichiers suivis.
- Rappel : ce fichier doit rester local et ne jamais entrer dans l’historique.

## 1.3. Petit changement simple
- Modifier le texte du `<h1>` dans `index.html` avec une nouvelle accroche.
- Vérifier les modifications ."Met à jour le titre principal de la page"
- Ajouter le fichier modifié et créer une sauvegarde.

---

# NIVEAU 2 – Remote principal, push/pull

## 2.1. Créer le dépôt distant “origin”
- Une seule personne crée un dépôt distant vide.
- Relier le projet local au dépôt distant.
- Vérifier la configuration du remote.
- Envoyer l’historique local vers le dépôt.

## 2.2. Clonage par le 2ᵉ stagiaire
- Cloner le dépôt à distance.
- Vérifier que les fichiers du projet sont présents, sauf le fichier TODO ignoré.

---

# NIVEAU 3 – Branches & modifications front simples

## 3.1. Création de branches
- Dev 1 crée une branche `feature-services`.
- Dev 2 crée une branche `feature-temoignages`.

## 3.2. Travail Dev 1 – section Services
- Ajouter un nouvel article dans la section Services dans `index.html`.
- (Option) Modifier légèrement le style des cartes dans `styles.css`.
- Sauvegarder les changements.

## 3.3. Travail Dev 2 – section Témoignages
- Ajouter un 4ᵉ témoignage dans la section Testimonials.
- Sauvegarder les changements.

## 3.4. Fusion des branches dans main
- Chacun envoie sa branche.
- Revenir sur `main`, récupérer les dernières modifications, puis fusionner successivement les deux branches.
- Résoudre les conflits si nécessaire et valider la fusion.

---

# NIVEAU 4 – 2 remotes (backup), fetch & push

## 4.1. Ajouter un remote de backup
- Créer un 2ᵉ dépôt distant pour la sauvegarde.
- Ajouter un remote secondaire nommé `backup`.
- Vérifier que `origin` et `backup` sont bien configurés.

## 4.2. Pousser vers les deux remotes
- Envoyer la branche principale vers `origin`.
- Envoyer la même branche vers `backup`.

## 4.3. Utiliser git fetch
- Un stagiaire pousse une modification sur `origin`.
- L’autre récupère les modifications à distance et compare l’historique.
- Intégrer ensuite ces changements.

---

# NIVEAU 5 – Conflits de merge

## 5.1. Provoquer un conflit
- Dev 1 modifie le paragraphe du hero dans `index.html`, enregistre et fusionne dans `main`.
- Dev 2 modifie le même paragraphe différemment, puis tente de fusionner après avoir récupéré `main`.
- Conflit attendu : il faut choisir une version ou fusionner les deux textes.
- Sauvegarder et envoyer les modifications.

---

# NIVEAU 6 – reset & revert

## 6.1. reset --soft
- Faire deux commits successifs.
- Revenir d’un commit tout en gardant les modifications prêtes à être enregistrées.
- Recréer un commit propre avec un meilleur message.

## 6.2. reset --mixed
- Ajouter plusieurs fichiers.
- Annuler uniquement la mise en staging, mais conserver les modifications.
- Ajouter uniquement un fichier et le valider.

## 6.3. reset --hard
- Modifier fortement le CSS.
- Annuler complètement toutes les modifications locales et revenir à l’état du dernier commit.

## 6.4. revert
- Choisir un commit ancien.
- Le revert crée un nouveau commit qui annule l’ancien sans modifier l’historique existant.
- Envoyer les changements.

