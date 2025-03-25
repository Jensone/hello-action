# Hello Action

C'est une action simple pour GitHub pour apprendre à publier ses propres actions.

## Structure d'exemple

- `action.yaml` : fichier décrivant l'action
- `index.js` : fichier principal de l'action
- `package.json` : fichier de dépendances
- `README.md` : fichier de description

## Utilisation

Pour l'utiliser, créer un fichier `.github/workflows/main.yml` avec le contenu suivant:

```yaml
name: Hello Action
on:
  push:
    branches:
      - main
jobs:
  hello:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: <nom-utilisateur>/hello-action@v1
        with:
          name: Martin
```