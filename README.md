[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/haifazrelli/tweets_classification.git/main?filepath=tweets_classifier.ipynb)
# tweets_classification
### Classification des Tweets
#  Introduction
La langue dans sa forme originale ne peut pas être traitée avec précision par une machine. Vous devez donc la traiter pour la rendre plus facile à comprendre. Pour donner un sens aux données, la première étape consiste à utiliser un processus appelé tokenization ou à scinder des chaînes en parties plus petites appelées tokens.

Un jeton est une séquence de caractères dans le texte qui sert d’unité. Selon la manière dont vous créez les jetons, ceux-ci peuvent être constitués de mots, d’émoticônes, de hashtags, de liens ou même de caractères individuels. Un moyen simple de diviser le langage en jetons consiste à scinder le texte en fonction des espaces et de la ponctuation.
objectifs:

Maitriser l’API de twitter pour l’extraction des tweets
Maitriser la partie NLP (natural language processing) avec NLTK en Python
Appliquer les principes de nettoyage des données
Classer les tweets : regrouper ensemble les tweets qui sont similaires.

on commence par l'extraction des tweets par les tokens
```js
import tweepy
consumer_key = "wXXXXXXXXXXXXXXXXXXXXXXX1"
consumer_secret = "qXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXh"
access_token = "9XXXXXXXX-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXi"
access_token_secret = "kXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXT"
```
```js
# Creating the authentication object
auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
# Setting your access token and secret
auth.set_access_token(access_token, access_token_secret)
# Creating the API object while passing in auth information
api = tweepy.API(auth)
```
## 1. Configurer les packages nécessaires

dans ce projet on a besoin d'importer queleques bibliotheques:

tweepy:Bibliothèque Python qui permet d’utiliser une API Twitter pour streamer les tweets

 numpy : permet d’effectuer des calculs numériques avec Python. Elle introduit une gestion facilitée des tableaux de nombres.
 
matplotlib.pyplot : est une collection de fonctions qui font fonctionner matplotlib comme MATLAB. Chaque fonction pyplot modifie une figure: par exemple, crée une figure, crée une zone de traçage dans une figure, trace des lignes dans une zone de traçage, décore le tracé avec des étiquettes, etc.

pandas : Pandas est une bibliothèque écrite pour le langage de programmation Python permettant la manipulation et l'analyse des données. Elle propose en particulier des structures de données et des opérations de manipulation de tableaux numériques et de séries temporelles.

NLTK en Python pour toutes les tâches NLP de ce tutoriel. Dans cette étape, vous allez installer NLTK et télécharger les exemples de tweets que vous utiliserez pour former et tester votre modèle.

 ## 2.Nettoyage des tweets
 
Les tweets contiennent des objets inutiles tels que des hashtags, des mentions, des liens et des signes de ponctuation qui peuvent affecter les performances d'un algorithme et doivent donc être supprimés. Tous les textes sont convertis en minuscules pour éviter que les algorithmes n'interprètent les mêmes mots avec des cas différents comme différents.
3.Traitement des tweets : NLP (Natural LanguageProcessing)

le package NLTK en Python pour toutes les tâches NLP . Dans cette étape, on commence par installer NLTK et télécharger les exemples de tweets qu'on utilise pour former et tester le modèle.

#### a.Tokenization :

#### b.supprimer Stop Words

#### c.Normalisation des mots
#### d. analyse des sentiments

#### c.Visualisation des résultats

### 4. Classification des tweets

KMeans qui est un algorithme de clustering de données non supervisé classique. En un mot, K-means utilise k centroïdes (points qui sont le centre d'un cluster) pour définir les clusters. Un point de données est considéré comme faisant partie d'un cluster particulier s'il est plus proche du centre de gravité de ce cluster que de tout autre centre de gravité

## Conclusion:

Dans ce projet j'ai appris à récupérer des informations à partir d'une API twitter et j'ai également appris à gérer les données recuperées , d'analyser ces données et d'extraire  des sentiments grâce à Natural Language Processing et dedeterminer des clusters par l'algorithme KMeans .
#### Dependances:
numpy == 1.18.5
matplotlib == 3.2.2
py == 1.9.0
scikit-learn == 0.23.1
scipy == 1.5.0
seaborn == 0.10.1
statsmodels == 0.11.1
pandas == 1.0.5
ipywidgets == 7.5.1
ipython == 7.16.1
glob2 == 0.7
nltk == 3.5
tweepy == 3.9.0
wordcloud == 1.8.1
