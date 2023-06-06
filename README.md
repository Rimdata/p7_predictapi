# OC Projet 7 - Implémentez un modèle de scoring
**Prêt à dépenser** est une société financière qui propose des crédits à la consommation pour des personnes ayant peu ou pas du tout d'historique de prêt.
L’entreprise souhaite mettre en œuvre un outil de “scoring crédit” pour calculer la probabilité qu’un client rembourse son crédit, puis classifie la demande en crédit accordé ou refusé. Elle souhaite donc développer un algorithme de classification en s’appuyant sur des sources de données variées. Cet algorithme implémentera un Dashboard interactif à travers d'une API de prédiction pour expliquer de façon la plus transparente possible les décisions d’octroi de crédit.

Liens vers les répertoires Github de ce projet:
* Les notebooks du projet : https://github.com/Rimdata/Implementez_un_modele_de_scoring
* L'API de prédiction : https://github.com/Rimdata/p7_predictapi
* Le Dashboard : https://github.com/Rimdata/P7_creditapp

# API de prédiction de remboursement de crédit

L'api est en ligne sur https://predictapi.herokuapp.com/

Ce répertoire GitHub contient une API permettant de prédire la probabilité de remboursement d'un crédit et de classifier le client en tant que client à risque ou client fiable, ainsi que de déterminer si la demande de crédit est accordée ou refusée. Ces prédictions sont basées sur un modèle de machine learning LightGBM classifier, qui est entraîné à partir des données clients.

## Comment utiliser l'API
Pour utiliser cette API, vous devez envoyer une requête HTTP POST à l'URL de l'API avec les données du client en tant que corps de la requête.
Les données client doivent être fournies au format JSON. 

L'API renverra une réponse au format JSON contenant la probabilité de remboursement, la classification du client (à risque ou fiable) et les shap values qui permetteront d'expliquer la décision prise.

## Pour le bon fonctionnement de l'API

* predictapi.py : code Python de l'API Flask
* requirements.txt : un fichier listant les packages utilisés 
* lgbm_model.pkl : le modèle préentrainé de prédiction basé sur l'algorithme de LightGBM classifier
* test_app.py : code Python avec les tests unitaires 
* Procfile
