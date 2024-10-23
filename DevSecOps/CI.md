# Intégration continue (CI)

L'intégration continue est la pratique de contrôle qualité automatique de l'application, effectuée typiquement à chaque commit ou pull/merge request.

Validations à inclure dans chaque CI :

- exécution des tests (unitaires, intégration, end-to-end)
  - Attention particulière portée à la partie API et authentification
  - Avoir un scenario complet "standard" en test end-to-end
- vérification du formattage du code
- lint : recherche des erreurs automatique dans le code
- qualité de code : SonarQube
    - code smells
    - duplciation
    - complexité 
    - security hotspots
- mises à jour régulières des dépendances (notamment bugs fixs et failles de sécurité) et utilisation d'un outil (par ex SocketSecurity dans le monde javascript) pour vérifier les vulnérabilités des dépendances utilisées.
