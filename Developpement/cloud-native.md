# Application cloud native

Il s'agit d'une application qui suit un certain nombre de principes et prérequis afin de pouvoir être déployée dans le cloud.

- [12-factor app](https://12factor.net/fr/)
- [15 factors](https://developer.ibm.com/articles/15-factor-applications/#the-additional-factors-and-why-they-are-important1)


## Application conteneurisée

- l'application doit être livrée via des images Docker
- en local, l'environnement de développement complet doit utiliser docker compose. Le lancement complet de l'environnement doit se faire par un simple `docker compose up`.
- en intégration / préproduction / production, la priorité est donnée au déploiement sur un cluster Kubernetes. A défaut, docker compose doit être utilisé si le déploiement se fait sur des VM.

## Migrations de données réversibles

Indispensable s'il est nécessaire de re déployer une ancienne version (rollback).

## Pré-requis de l'équipe technique produit

- Gestion de configuration et définition claire de la gestion des branches git (feature, intégration, preproduction). Les tags sont utilisés pour la production
- Validation par les pairs lors de revue de code (merge/pull request)
- Refacto en continu pour limiter la dette technique
- Homogénéisation des pratiques au sein de l'organisation (facilite la réversibilité interne)
- Cadre de cohérence technique
