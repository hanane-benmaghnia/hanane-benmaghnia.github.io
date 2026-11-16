# Mon site de chercheuse ✿ / My researcher website

Site statique bilingue (anglais + français), HTML + CSS sans dépendance, prêt pour GitHub Pages.
Thème rose vif et lavande.

## Structure

```
index.html            # choix de la langue (redirection automatique selon le navigateur)
style.css             # styles communs (couleurs en variables en haut du fichier)
en/                   # version anglaise
  index.html          #   Home
  research.html       #   Research
  publications.html   #   Publications
  teaching.html       #   Teaching
  contact.html        #   Contact
fr/                   # version française (mêmes pages : Accueil, Recherche, ...)
assets/
  photo.jpg           # votre portrait (carré de préférence)
  cv.pdf              # votre CV
```

Chaque rubrique a sa propre page, et le bouton **EN | FR** en haut à droite
renvoie vers la même page dans l'autre langue.

## Mise en ligne sur GitHub Pages

1. Créez un compte sur https://github.com.
2. Créez un dépôt **public** nommé exactement `votre-pseudo.github.io`.
3. Déposez-y tout le contenu de ce dossier (y compris `en/`, `fr/` et `assets/`) :
   - via l'interface web : *Add file → Upload files* (glissez le contenu décompressé), ou
   - en ligne de commande :
     ```bash
     git clone https://github.com/votre-pseudo/votre-pseudo.github.io
     cd votre-pseudo.github.io
     # copiez les fichiers ici
     git add .
     git commit -m "Première version de mon site"
     git push
     ```
4. Dans le dépôt : *Settings → Pages → Build and deployment*, choisissez
   **Deploy from a branch**, branche `main`, dossier `/ (root)`.
5. Après une à deux minutes, le site est en ligne sur `https://votre-pseudo.github.io`.

## Personnalisation

- Remplacez tous les textes entre crochets `[...]` et les liens d'exemple
  (Scholar, ORCID, HAL, e-mail, GitHub) dans **les deux dossiers** `en/` et `fr/`.
  Astuce : une recherche/remplacement dans tout le dossier (par exemple `first.last@university.edu`)
  évite d'oublier des pages.
- Ajoutez `assets/photo.jpg` et `assets/cv.pdf`. Sans photo, le portrait est masqué
  automatiquement ; retirez le bouton « CV » si vous n'avez pas de fichier.
- Couleurs : variables `--pink`, `--pink-deep`, `--lavender` en haut de `style.css`.
- Pour ajouter une rubrique : copiez une page (par exemple `research.html`) dans `en/` et `fr/`,
  puis ajoutez le lien dans la barre de navigation de chaque page.

## Tester en local

```bash
python3 -m http.server 8000
# puis ouvrez http://localhost:8000
```
