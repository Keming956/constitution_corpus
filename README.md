# Introduction :
1. je vais travailler sur la traduction
2. https://huggingface.co/datasets/ted_talks_iwslt
3. traduire automatique les sous-titres, avec machine translation
4. Models trained or fine-tuned on ted_talks_iwslt
5. Ce corpus est une collenction du Ted talks et leur traduction faite par des volontaires, disponible dans plus de 109 langues. Par conséquent, c'est un corpurs traité pour la tâche de traduction, sous-tâche maching translation.



# Difficulté :

1. Les transcriptions récupérés sur le site TedTalk ne sont pas alignés, donc j’ai dû utiliser Matecat pour les aligner sous forme `tmx`, mais les résultats ne sont pas satisfaisants. Mais si je le fais manuellement, cela me prendre trop de temps et je crois que ce n’est pas le but de ce cours non plus. D’ailleurs, j’ai abandonné sur les transcriptions chinoises car c’est encore plus dûr de faire l’alignement entre 3 langues. Évidemment, ce corpus n’est pas de haute qualité.

2. Pour augmenter les donées, je n’ai pas réussi, le modèle RoBERTa génère toujours les mêmes phrases. Donc j’ai utilisé un autre modèle `Marian` pour faire la retraduction. Mais je n’ai pas augmenté tout le corpus mais que les 100 premiers lignes car cela prend trop de temps sur mon ordinateur, je n’ai pas terminé l’augmentation d’anglais pour 1 h. Étant donné que mon corpus n’est pas bien aligné, donc je sais que les scores seront assez bas, c’est pourquoi j’ai juste testé l’augmentation sur une petite partie du corpus. Par rapport au split du corpus, j’ai splitté celui d’originel car le corpus augmenté est petit.

   

# Datacard 

### Data Summary

This corpus is a collection of the orginal Ted talks and their translated version in French.

### Supported Tasks

machine translation, language modeling and generation

### Language

English and French

### Datastructure

One exemple from the dataset is:

```json
{"en": "People are feeling overwhelmed.", "fr": "Que c'est trop de technologie, trop vite."}
```

### **Data Fields**

en: The English transcription

fr: The French translation of the English text

### Date split

The dataset is split into three parts:

​	•	Train: 80% of the data

​	•	Dev: 10% of the data

​	•	Test: 10% of the data

### Dataset Creation

The talks were collected from the [Ted Conference website](http://www.ted.com/)
