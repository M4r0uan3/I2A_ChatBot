# I2A_ChatBot

- https://drive.google.com/drive/folders/1OA9-vcGwkqEwtUttzq-UJdJO4BJpErHl?usp=drive_link

# test:
```
- I love you
- I hate LLM
- track_name: All the Day (Don Rokoko Remix)
- ner <something>
```

# Fonction sentiment_analysis

Effectue une analyse de sentiment sur le texte fourni en utilisant un modèle spécifique.

## Paramètres

- `text` (str) : Le texte d'entrée pour l'analyse de sentiment.

## Renvoie

- Renvoie un tuple contenant :
  - Un sentiment potentiel proche de celui d'un être humain (str) en cas de succès.
  - Un score de confiance (float) indiquant la confiance du modèle dans le sentiment prédit.

Si la fonction rencontre une erreur pendant l'exécution, elle renvoie `None` pour les deux valeurs.

## Lève

- `ValueError` : Si le texte d'entrée (`text`) est vide ou `None`.


## Utilisation
```python
Enter your query: i love you 
```
## Exemple de sortie

```python
Sentiment: The text reflects a positive sentiment.
```

## Notes

- La fonction utilise le modèle "finiteautomata/bertweet-base-sentiment-analysis" pour l'analyse de sentiment.
- Le label de sentiment est associé à des réponses potentiellement proches de celles d'un être humain pour une meilleure compréhension.
- La fonction gère les exceptions et affiche toute erreur rencontrée.

---- 

# Fonction music_style

## Utilisation

```yml
Enter your query: track_name: All the Day (Don Rokoko Remix)
```
Assuming the model predicts the genre as 'Pop', the output will be:

```python
Predicted Genre: Pop
```


---
# Fonction de Reconnaissance des Entités Nommées (NER)

Cette fonction réalise la Reconnaissance des Entités Nommées (NER) sur le texte donné en utilisant un modèle BERT pré-entraîné ajusté pour le jeu de données CoNLL-03 en anglais.

## Paramètres

- `text` (str) : Le texte d'entrée sur lequel la NER sera effectuée.

## Renvoie

- Renvoie une liste des entités identifiées dans le texte d'entrée.



