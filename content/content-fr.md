Les transform‚es de Fourier sont un outil utilis‚ pour tout un tas de trucs diff‚rents. Ceci est une explication de ce que fait une transform‚e de Fourier, et de diff‚rentes maniŠres dont elle peut ˆtre utile. Et comment vous pouvez cr‚er de belles choses avec, comme celle-ci?:

<canvas id="self-draw" class="sketch" width=500 height=500></canvas>

Je vais expliquer comment cette animation fonctionne, et en mˆme temps expliquer les transform‚es de Fourier?!

A la fin vous devriez avoir une id‚e assez bonne de?:
- ce que fait une transform‚e de Fourier?;
-?Quelques usages pratiques des transform‚es de Fourier?;
-?Quelques usages inutiles mais chouettes des transform‚es de Fourier.

Nous laisserons les maths et les ‚quations de c“t‚ pour le moment. Il y a un paquet de maths int‚ressantes derriŠre, mais il vaut mieux commencer par ce que ‡a fait en r‚alit‚, et pourquoi vous voulez vous en servir au d‚part. Si vous voulez en savoir plus sur le comment, il y a e

## Alors c'est quoi cette chose??

Dit simplement, la transform‚e de Fourier est un moyen de d‚couper quelque chose en un tas d'ondes sinuso‹dales. Comme d'habitude, le nom vient d'une personne qui a v‚cu il y a longtemps et qui s'appelait Fourier.

Commen‡ons par quelques exemples simples et avan‡ons progressivement. D'abord, nous allons regarder les ondes?- des motifs qui se r‚pŠtent avec le temps.

Voici un exemple d'onde?:

<canvas id="combo-sine-wave" class="sketch" width=500 height=300></canvas>

Ce motif ondul‚ peut ˆtre d‚coup‚ en ondes sinuso‹dales. C'est-…-dire que quand on ajoute les deux ondes sinuso‹dales, on obtient … nouveau l'onde originale.

<canvas id="combo-sine-wave-split" class="sketch" width=500 height=500></canvas>

La transform‚e de Fourier est un moyen pour nous de prendre l'onde combin‚e, et d'en obtenir chacune des ondes sinuso‹dales s‚par‚ment. Dans cet exemple, vous pouvez presque le faire dans votre tˆte, rien qu'en regardant l'onde originale.

Pourquoi?? Il se trouve qu'un grand nombre de choses du monde r‚el interagissent sur la base d'ondes sinuso‹dales. En g‚n‚ral, on les appelle les fr‚quences de l'onde.

L'exemple le plus ‚vident est le son?- quand on entend un son, on n'entend pas cette ligne ondul‚e, on entend les diff‚rentes fr‚quences des ondes sinuso‹dales qui composent le son.


<button id="together-button" class="button">Play Full Wave</button>

<button id="split-button-1" class="button">Play High Frequency</button>

<button id="split-button-2" class="button">Play Low Frequency</button>

La capacit‚ de les d‚composer … l'aide d'un ordinateur nous donne une compr‚hension de ce qu'une personne entend en r‚alit‚. On peut comprendre qu'un son est grave ou aigu, ou d‚terminer de quelle note il s'agit.

On peut ‚galement utiliser ce proc‚d‚ sur des ondes qui n'ont pas l'air d'ˆtre compos‚es de sinuso‹des.

Jetons un oil … ce petit gars. On appelle ‡a une onde carr‚e.

<canvas id="square-wave" class="sketch" width=500 height=300></canvas>

Elle n'en a pas l'air, mais elle peut ‚galement ˆtre d‚coup‚e en ondes sinuso‹dales.

<canvas id="square-wave-split" class="sketch" width=500 height=500></canvas>

Il nous en faut beaucoup cette fois -?techniquement, une infinit‚ pour la repr‚senter parfaitement. A mesure que nous ajoutons de plus en plus de sinuso‹des, le motif se rapproche de plus en plus de l'onde carr‚e de d‚part.

<canvas id="square-wave-build-up" class="sketch" width=500 height=500></canvas>
<input id="square-wave-build-up-slider" type="range" min="0" max="1" value="0" step="any" >

<button id="square-wave-button" class="button">Play Wave</button>

*D‚placez le curseur ci-dessus pour jouer avec la quantit‚ de sinuso‹des.*

Visuellement, vous noterez qu'en r‚alit‚, les premiŠres sinuso‹des sont celles qui font la plus grande diff‚rence. Avec le curseur … mi-chemin, on a la forme g‚n‚rale de l'onde, mais elle est toute ondul‚e. On a juste besoin des petites ondes restantes pour aplatir les ondulations.

Quand vous ‚coutez l'onde, vous entendez le son devenir plus grave, car on supprime les fr‚quences les plus hautes.

Ce proc‚d‚ fonctionne ainsi pour n'importe quelle ligne qui se r‚pŠte. Allez-y, essayez de dessiner votre propre onde?!

<div class="multi-container">
<div class="sketch" >
    <canvas id="wave-draw" class="sketch-child" width=500 height=300></canvas>
    <p id="wave-draw-instruction" class="instruction wave-instruction">Dessinez ici?!</p>
</div>
<canvas id="wave-draw-split" class="sketch" width=500 height=500></canvas>
</div>
<input id="wave-draw-slider" type="range" min="0" max="1" value="1" step="any">
<button id="wave-draw-button" class="button">Jouer l'onde</button>

*D‚placez le curseur pour voir comment, … mesure qu'on ajoute des sinuso‹des, ‡a devient de plus en plus proche de votre dessin*
































