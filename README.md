# Diamond System – Billard 3 bandes

Application web pour comprendre le Diamond System du billard français 3 bandes :
valeurs d'arrivée, de départ, de visée et trajet avec rebond (incidence = réflexion).
Elle s'installe sur l'écran d'accueil de l'iPhone et fonctionne ensuite sans connexion.

## Contenu du dossier

| Fichier | Rôle |
| --- | --- |
| `index.html` | L'application (une seule page) |
| `manifest.webmanifest` | Nom, icônes et affichage plein écran |
| `sw.js` | Mode hors ligne |
| `icons/` | Icônes de l'application |
| `.nojekyll` | Facultatif : dit à GitHub Pages de publier les fichiers tels quels (fichier caché) |

## Publier sur GitHub Pages

À faire depuis un ordinateur : l'envoi d'un dossier avec ses sous-dossiers est difficile depuis un téléphone.

1. Sur github.com, créez un compte, puis un nouveau dépôt public, par exemple `diamond-system`.
2. Dans le dépôt, choisissez **uploading an existing file**, puis glissez-y **tout le contenu** de ce dossier
   (`index.html`, `manifest.webmanifest`, `sw.js` et le dossier `icons` ; le fichier `.nojekyll` est facultatif). Validez avec **Commit changes**.
3. Ouvrez **Settings → Pages**. Dans « Build and deployment », choisissez
   **Deploy from a branch**, la branche **main** et le dossier **/ (root)**, puis **Save**.
4. Après une minute environ, l'adresse s'affiche en haut de la page :
   `https://<votre-nom-utilisateur>.github.io/diamond-system/`
   (par exemple `https://diamond3c.github.io/diamond-system/`).

## Installer sur iPhone

1. Ouvrez l'adresse dans **Safari** (pas dans un autre navigateur).
2. Touchez le bouton **Partager**, puis **Sur l'écran d'accueil**, puis **Ajouter**.
3. Lancez l'application depuis son icône. Une fois ouverte une première fois avec internet, elle marche hors ligne.

## Mettre à jour

Remplacez `index.html` dans le dépôt. La page se met à jour toute seule dès que l'iPhone a internet.
Si vous modifiez une icône ou le manifeste, changez aussi le numéro de version dans `sw.js`
(`diamond3c-v1` devient `diamond3c-v2`) pour forcer le rafraîchissement.

## Tester sur votre ordinateur

Dans ce dossier, lancez `python3 -m http.server 8000`, puis ouvrez `http://localhost:8000`.
Le mode hors ligne ne fonctionne que sur `localhost` ou en `https`, pas en ouvrant le fichier directement.

## À savoir

- La police (Bricolage Grotesque) est chargée depuis Google Fonts au premier lancement, puis gardée en mémoire.
  Si la première ouverture se fait sans internet, l'application utilise la police du téléphone.
  Pour l'embarquer, placez les fichiers de police dans le dépôt et remplacez le lien Google Fonts dans `index.html`.
- Ce dépôt n'a pas de licence. Ajoutez-en une (bouton **Add file → Create new file → LICENSE**) si vous voulez
  autoriser la réutilisation du code.
