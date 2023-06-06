# Projet 7 - Openclassrooms
# Implémentez un modèle de scoring
# API de prédiction de remboursement de crédit

L'api est en ligne sur https://predictapi.herokuapp.com/

Ce répertoire GitHub contient une API permettant de prédire la probabilité de remboursement d'un crédit et de classifier le client en tant que client à risque ou client fiable, ainsi que de déterminer si la demande de crédit est accordée ou refusée. Ces prédictions sont basées sur un modèle de machine learning LightGBM classifier, qui est entraîné à partir des données clients.

## Comment utiliser l'API
Cette API est appelée par le dashboard 

Pour utiliser cette API, vous devez envoyer une requête HTTP POST à l'URL de l'API avec les données du client en tant que corps de la requête.
Les données client doivent être fournies au format JSON. 

L'API renverra une réponse au format JSON contenant la probabilité de remboursement, la classification du client (à risque ou fiable) et les shap values qui permetteront d'expliquer la décision prise.
