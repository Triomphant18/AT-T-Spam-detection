# AT&T Spam Detector

## **Contexte**
Les utilisateurs d'AT&T sont constamment exposés à des messages indésirables (SPAM), qui nuisent à leur expérience utilisateur et peuvent contenir des contenus nuisibles ou frauduleux. Ce projet vise à développer un détecteur de SPAM automatisé basé sur du deep learning, capable de classer les SMS en SPAM ou HAM (légitimes).

## **Objectif**
Créer un modèle capable d'identifier automatiquement les messages SPAM grâce à une approche basée sur le contenu des SMS.

## **Données**
Le projet utilise un ensemble de données contenant des SMS étiquetés comme SPAM ou HAM. Les étapes de prétraitement incluent le nettoyage des textes, la lemmatisation, et la suppression des stop words.

## **Bibliothèques utilisées**
### **1. Manipulation des données**
- **`numpy`** : Manipulation efficace des tableaux.
- **`pandas`** : Gestion et exploration des données textuelles.

### **2. Visualisation des données**
- **`matplotlib`** : Création de visualisations statiques.
- **`seaborn`** : Visualisations pour comprendre la répartition des données.
- **`plotly`** : Création de graphiques interactifs.
- **`WordCloud`** : Génération de nuages de mots pour explorer les termes fréquents.

### **3. Traitement du langage naturel (NLP)**
- **`spacy`** : 
  - Analyse et traitement des textes en anglais.
  - Suppression des stop words et lemmatisation.
  - Utilisation du modèle linguistique **`en_core_web_sm`**.

### **4. Modélisation**
- **`tensorflow.keras`** : Chargement et gestion des modèles de deep learning.
- **`torch` (PyTorch)** : Utilisé pour le transfert d'apprentissage à partir de modèles pré-entraînés.

### **5. Encodage des étiquettes**
- **`LabelEncoder`** : Transformation des étiquettes textuelles en valeurs numériques.

## **Approche**
1. **Prétraitement des textes**
   - Conversion des textes en minuscules.
   - Suppression des espaces inutiles, URL, émojis et adresses e-mail.
   - Nettoyage des caractères spéciaux et lemmatisation.
2. **Exploration des données**
   - Visualisation des termes fréquents avec des nuages de mots.
   - Analyse de la répartition des classes SPAM et HAM.
3. **Modélisation**
   - Entraînement d'un ou plusieurs modèles de deep learning.
   - Utilisation de modèles pré-entraînés avec PyTorch pour améliorer les performances.
4. **Évaluation**
   - Utilisation des métriques telles que la précision, le rappel, le F1-score et l'accuracy.

## **Livrables**
- Un notebook contenant :
  - Le prétraitement des données.
  - L'entraînement des modèles avec comparaison des performances.
  - L'évaluation des modèles avec des métriques appropriées.
- Des visualisations claires pour appuyer l'analyse des résultats.

## **Installation**
Pour exécuter ce projet, les bibliothèques suivantes doivent être installées :
```bash
pip install numpy pandas matplotlib seaborn plotly wordcloud spacy tensorflow torch scikit-learn
```
Assurez-vous également de télécharger et charger le modèle linguistique **Spacy** :
```bash
python -m spacy download en_core_web_sm
```

## **Conclusion**
Ce projet vise à automatiser la détection des spams en exploitant les techniques de NLP et de deep learning. Une solution efficace permettra d'améliorer l'expérience utilisateur en réduisant l'exposition aux contenus indésirables.
