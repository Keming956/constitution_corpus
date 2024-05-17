# Introduction :
1. je vais travailler sur la traduction
2. https://huggingface.co/datasets/ted_talks_iwslt
3. traduire automatique les sous-titres, avec machine translation
4. Models trained or fine-tuned on ted_talks_iwslt
5. Ce corpus est une collenction du Ted talks et leur traduction faite par des volontaires, disponible dans plus de 109 langues. Par conséquent, c'est un corpurs traité pour la tâche de traduction, sous-tâche maching translation.



# Difficulté :

1. Les transcriptions récupérés sur le site TedTalk ne sont pas alignés, donc j’ai dû utiliser Matecat pour les aligner sous forme `tmx`, mais les résultats ne sont pas satisfaisants. Mais si je le fais manuellement, cela me prendre trop de temps et je crois que ce n’est pas le but de ce cours non plus. D’ailleurs, j’ai abandonné sur les transcriptions chinoises car c’est encore plus dûr de faire l’alignement entre 3 langues. Évidemment, ce corpus n’est pas de haute qualité.
