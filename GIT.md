# Git repos for ML at Ynov, Spring 2019.

Ajouter le liens à votre repo git avec texte qui vous identifie.
Tenir en ordre lexicographique par nom.

Vous voulez tous cloner ? Rien n'est plus simple. Dans un nouveau
répertoire non-contrôlé par git, tapez le suivant :

```
grep https /path/to/GIT.md | \
    tr -d '[]()'           | \
	sed -e 's/\(^.*https\)\(.*$\)/https\2::\L\1/;  s/https$//; s/ /-/g; s/::/  /; s/^/git clone /;'
```

## Les répertoires à créer (projets)

### Contrôles Continus

_Répertoire : ContrôleContinu_

Pour les contrôles continus qui sont en code. Créez des fichiers avec
noms clairs pour chaque contrôle (ou créez un sous-répertoire, au choix).

### MNIST

_Répertoire : TP1_MNIST_

Utiliser une régression logistique (disponible dans scikit-learn) pour
construire un classifieur, et OvO et OvA, sur le jeu de données MNIST.

### Le logarithme naturel

_Répertoire : TP2_logarithme_

1.  Écrire un programme qui calcule la valeur de $e$ en utilisant la
    série de Taylor, montrant la convergence de la série.

2.  Écrire un programme qui calcule le facteur (exprimé comme une
    limite) dans la dérivé de $n^x$.

### Recommendation

_Répertoire : TP3_recommandation_

Utiliser le jeu de données MovieLens pour créer un moteur de
recommendation.

### CART

_Répertoire : TP4_CART_

Refaire MNIST avec une random forest et avec SVM (+rbf). Faire une
comparaison des techniques : régression logistique (OvO, OvA), CART,
et SVM.

### CART, variation du 17 avril 2019

_Répertoire : TP4_CART++_

En cours le 17 avril 2019 nous allons regarder ensemble des jeux de
données
[ici](https://scikit-learn.org/stable/datasets/index.html#real-world-datasets),
avec objectif de faire la même exercice que proposé la semaine
précédente. Si vous voulez, vous pouvez télécharger avant de venir au
cours. Vous terminerez cet exercice pour la semaine suivante.

En cours, nous nous diviserons en groupe de deux, et chaque groupe
aura son propre jeu de données. Pour la semaine prochaine, vous
terminerez indépendemment.

### Perceptron

Vous allez mettre en oeuvre un perceptron, dont vous vous servirez
pour faire une reconnaissance de MNIST.  Vous pouvez utilisez des
libraries comme numpy et scipy mais pas scikit-learn.  Si vous voulez
tester votre travail, vous pouvez répéter le tout avec
[`sklearn.linear_model.Perceptron`](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Perceptron.html).

Comme d'habitude, vous devez tester votre travail avec
`train_test_split`.  Afin de ne pas fournir un résultat aberrant, il
faut faire plusieurs `train_test_split`.  Vous pourriez trouver que
[`cross_validate`](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.cross_validate.html)
et
[`cross_val_score`](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.cross_val_score.html)
intéressants.  Une discussion se trouve
[ici](https://scikit-learn.org/stable/modules/cross_validation.html).

Ajouter à votre tableau de comparaison de méthodes ce que vous aurez
fait avec perceptron.

### MLP et RNN

Pour la dernière séance, mettez en oeuvre un MLP et un RNN pour MNIST.
Afin que cela soit plutôt raisonnable, voilà quelques codelabs avec le
code quasiment complet :

* [MLP](https://github.com/keras-team/keras/blob/master/examples/mnist_mlp.py)
* [CNN](https://github.com/keras-team/keras/blob/master/examples/mnist_cnn.py)

Pour un peu plus de détail, il existe ce
[codelab](https://www.tensorflow.org/tutorials/estimators/cnn) et
[ipynb sur
git](https://github.com/tensorflow/docs/blob/master/site/en/tutorials/estimators/cnn.ipynb).

Afin d'apprécier la simplification que propose Keras, regardez
également les [mêmes exercices en
TensorFlow](https://github.com/aymericdamien/TensorFlow-Examples) :
[MLP](https://github.com/aymericdamien/TensorFlow-Examples/blob/master/notebooks/3_NeuralNetworks/neural_network_raw.ipynb)
et [CNN](https://github.com/aymericdamien/TensorFlow-Examples/blob/master/notebooks/3_NeuralNetworks/convolutional_network.ipynb).


## Étudiants

[Tanguy Badier](https://github.com/Rock3f/Exercice-Machine-Learning)

[Florian Boche](https://github.com/Nair0fl/CoursMachineLearning)

[Benjamin Brasseur](https://github.com/benjaminbra/ML-BBR)

[Clément Caillaud](https://github.com/ClementCaillaud/MachineLearning_ynov)

[Benoît Cochet](https://github.com/BenoitCochet/ML)

[Maxime Courant](https://github.com/mcourant/ml-exo)

[Yanis Dando](https://github.com/Mokui/code_ML)

[Alexandre Desvallées](https://github.com/AlexDesvallees/Alex-ML)

[Antoine Drouard](https://github.com/Coblestone/ML-2019)

[Matthieu Fournier](https://github.com/LordInateur/ML_2019_matthieuf_exo)

[Guillaume Fourny](https://github.com/gfourny/Machine-Learning)

[Antoine Gosset](https://github.com/AntoineGOSSET/Machine-Learning)

[Nicolas Goureau](https://github.com/Killy85/MachineLearningExercises)

[Grégoire Meunier](https://github.com/Grigusky/ml_2019)

[Kevin Pautonnier](https://github.com/KevinPautonnier/MachineLearning.git)

[Thomas Pichard](https://github.com/thomaspich/MachineLearning)

[Matthieu Saint-Martin](https://github.com/msaintmartin/ml-exercises)

## Projets

Pour le projet final, vous vous composerez en groupe de deux (minimum)
à quatre (maximum) personnes afin de faire un projet que vous
présenterez vendredi 4 mai lors de la dernière séance. Vous pouvez
travailler sur n'importe quel projet qui vous semble bon si le
professeur est d'accord. Le projet par défaut est de construire un
système de reconnaissance de visage qui reconnaît les 18 personnes du
cours (y compris le prof).

Lors de votre présentation, vous devez expliquer ce que vous avez
fait, y compris son évolution. Par exemple, vous devriez expliquer la
première version du système, comment vous l'avez mesuré, et comment
vous l'avez amélioré.

Attention à ne pas vous laisser distraire par l'interface humaine.
Une IH est une bonne idée, mais un projet qui maîtrise parfaitement le
ML sans UI appréciable serait beaucoup mieux noté que le contraire.

Le choix du projet doit être convenu avant la fin du week-end initial
(7 avril) sauf dérogation explicite. Dans les premiers jours vous
devez créer un planning provisionnel de ce que vous compter faire (au
moins par semaine) avec des points de progrès clairement défini tel
que c'est possible d'évaluer s'ils sont achevés ou pas.

Quand vous achevez les points importants de progrès ou quand vous
auriez une question, vous devez créer un issue avec chacun dans
l'équipe ainsi que le professeur tagés afin que nous puissions
discuter votre progrès.

### [GATA](https://github.com/Rock3f/ML-Projet-GATA)

- Guillaume Fourny
- Alexandre Desvallées
- Tanguy Badier
- Antoine Gosset

Projet d'initiation à la reconnaissance faciale

### [Nikmabe](https://github.com/Killy85/game_ai_trainer)

- Nicolas
- Benjamin
- Kevin
- Matthieu Fournier

Project aiming at creating a bot able to play a game the best way
possible. Using reinforcement learning, we will create an agent and
make it learn our game.

### [FLANBENT](https://github.com/Nair0fl/ML-PROJECT.git)
* Antoine Drouard
* Benoît Cochet
* Clément Caillaud
* Florian Boche

Projet d'initiation à la reconnaissance faciale

### [NeuronalGates](https://github.com/Mokui/NeuronalGates)

- Yanis
- Grégoire

Little project to create neurons. This neurons aim to learn something from themselves

### [MYMETEO](https://github.com/mcourant/mymeteo-ml)
* Matthieu Saint-Martin
* Thomas Pichard
* Maxime Courant

Init project my meteo, predict the weather for 1 week
