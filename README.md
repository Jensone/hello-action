# Hello Action

C'est une action simple pour GitHub pour apprendre à publier ses propres actions.

## Structure d'exemple

- `action.yaml` : fichier décrivant l'action
- `entrypoint.sh` : fichier exécutable qui sera exécuté lors de l'exécution de l'action
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
      - uses: <nom-utilisateur>/hello-action@v1.x
        with:
          name: Martin
```