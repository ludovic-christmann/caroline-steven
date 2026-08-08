# Mise en ligne sur GitHub Pages

## Contenu du dossier

| Chemin | Version du faire-part |
|---|---|
| `8a3f1c7d/` | **Complet** — Mairie + Réception + Houppa/Soirée |
| `4b9e2d56/` | **Réception** seule (5 mars, Villa Quai Sturm) |
| `e70c5a92/` | **Houppa + Soirée** (28 mars, Boulogne + La Palmeraie) |
| `assets/` | Images partagées par les trois pages |
| `index.html` | Page neutre affichée si quelqu'un ouvre l'adresse racine |
| `404.html` | Même page, pour toute adresse inexistante |
| `robots.txt` | Demande aux moteurs de recherche de ne pas indexer |
| `.nojekyll` | Désactive le traitement Jekyll de GitHub Pages |

Les réponses RSVP partent vers **ludochristm@gmail.com**.
Date limite affichée : **X** — à remplacer, voir plus bas.

## Étapes

1. Créer un compte sur github.com si besoin.
2. Créer un dépôt **public** nommé `mariage` (Pages est payant sur les dépôts privés).
3. Sur la page du dépôt : `Add file` → `Upload files`, puis glisser **le contenu de ce dossier** (pas le dossier lui-même) : les 3 dossiers hexadécimaux, `assets/`, `index.html`, `404.html`, `robots.txt`.
   `.nojekyll` est invisible dans l'explorateur Windows — activer « Éléments masqués » dans l'onglet Affichage pour pouvoir le glisser.
4. `Commit changes`.
5. `Settings` → `Pages` → Source : **Deploy from a branch** → Branche `main`, dossier `/ (root)` → `Save`.
6. Attendre 1 à 2 minutes.

## Liens à envoyer aux invités

En remplaçant `PSEUDO` par ton nom d'utilisateur GitHub :

- Complet : `https://PSEUDO.github.io/mariage/8a3f1c7d/`
- Réception : `https://PSEUDO.github.io/mariage/4b9e2d56/`
- Houppa + Soirée : `https://PSEUDO.github.io/mariage/e70c5a92/`

Le `/` final est important.

## Modifier la date limite de réponse

La page affiche pour l'instant « Réponse souhaitée avant le X ».

Dans chacun des trois `index.html`, ouvrir le fichier dans un éditeur de texte (Notepad++, VS Code) et chercher :

```
deadline=\"X\"
```

Les guillemets sont bien précédés d'une barre oblique inverse — c'est normal, le contenu est encodé. Remplacer par exemple par :

```
deadline=\"1ᵉʳ février 2027\"
```

Le texte apparaît tel quel sur la page. À faire dans les trois fichiers.

## Domaine personnalisé (plus tard)

1. Acheter le domaine (OVH, Gandi, Namecheap…).
2. Chez le registrar, créer 4 enregistrements `A` sur `@` vers `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, et un `CNAME` sur `www` vers `PSEUDO.github.io`.
3. Sur GitHub : `Settings` → `Pages` → `Custom domain` → saisir le domaine → `Save`, puis cocher `Enforce HTTPS` une fois le certificat émis (quelques minutes à quelques heures).

Les liens deviennent alors `https://ton-domaine.fr/8a3f1c7d/` — plus courts, et les dossiers hexadécimaux restent valables.

## À savoir

- **Le site est public.** Les codes hexadécimaux ne sont pas devinables et le `noindex` évite Google, mais un invité qui partage son lien donne accès à sa version. Il n'y a pas de mot de passe possible sur un site statique.
- **Le RSVP utilise `mailto:`.** Le formulaire ouvre le logiciel de messagerie de l'invité avec le message pré-rempli ; il doit encore cliquer sur « Envoyer ». Sur mobile ça fonctionne bien ; sur un ordinateur sans client mail configuré, rien ne se passe. Si tu veux fiabiliser ça plus tard, un service comme Formspree ou Tally se branche en remplacement.
- **Mise à jour du site :** re-uploader les fichiers modifiés sur GitHub, la mise en ligne se refait toute seule en 1–2 minutes.
