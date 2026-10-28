# Pomodoro du chat rond

Une page web, un seul fichier (`index.html`). Tu choisis le moment, la météo et la durée (1h à 8h), tu cliques sur Démarrer, et tout s'enchaîne tout seul : travail, pauses, déjeuner. Tu mets ta propre musique à côté.

## Publier sur GitHub Pages

1. Crée un dépôt public sur GitHub (par exemple `pomodoro-chat`).
2. Envoie `index.html` et `README.md` dans ce dépôt.
3. Dans le dépôt : Settings, Pages, "Deploy from a branch", branche `main`, dossier `/ (root)`, Save.
4. Après une minute ou deux, la page est disponible à l'adresse `https://TON-PSEUDO.github.io/pomodoro-chat/`.

## Modifier le découpage

Dans `index.html`, cherche `SCHEDULES`. Chaque durée est une liste de segments :

- `cyc(n)` : n cycles de 25 min de travail + 5 min de pause eau
- `seg('tv', 15)` : une pause télé de 15 min
- `seg('work', 15)` : un dernier bloc de travail de 15 min
- `seg('lunch', 60)` : le déjeuner d'une heure

Les textes affichés dans "Découpage" sont dans `CUTS`.

## Bon à savoir

- **Veille de l'ordinateur** : le chrono suit l'heure réelle. Au réveil, il se recale tout seul sur la bonne phase, sans rejouer les sons manqués.
- **Sons** : générés par le navigateur, aucun fichier. Ils ne démarrent qu'après un clic sur Démarrer (règle des navigateurs). Un son pour le début du travail, un autre, plus lent et plus grave, pour la fin.
- **Garder l'écran allumé** : évite la veille de l'écran pendant la session. Il faut que l'onglet reste visible, et la page doit être en HTTPS (c'est le cas sur GitHub Pages).
- **Réglages** : le moment, la météo, la durée et l'option écran sont mémorisés dans le navigateur.
- **Onglet en arrière-plan** : le chrono continue, et le titre de l'onglet affiche le temps restant.
