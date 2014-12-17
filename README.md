# Dojo-13

Axa WebCenter Lille & Axa Nanterre

6 groupes à Lille (tous en c#), 1 groupe à Paris (tous en c#)

# Sujet
Le sujet d'aujourd'hui et le Kata de Refactoring 'Katastrophic' écrit par Eric Lemerdy : https://github.com/ericlemerdy/katastrophic/

Dans ce kata, nous avons 2 objectifs :
  * Comprendre ce que le code fait.
  * Rendre le code plus lisible sans en changer son comportement.

Nous avions 2h pour ce kata, découpé comme suis: 10-15 minutes d'explication du sujet, 1h30 de code, 20-25 minutes de debrief.
On se donne comme objectif lors du premier 1/4 d'heure de comprendre le sujet.

Au bout d'1/4 on a fait emerger avec le groupe qu'avec un code aussi hostile et incomprehensible, on pouvait aborder de la manière suivante:

* Vu qu'on ne comprends pas ce que cela fait, on tente de le faire tourner et de deverser à l'intérieur des données en entrées au petit bonheur la chance pour voir comme le programme réagit.
* On se rends compte assez vite que cela n'est pas vraiment suffisant il est difficile de deviner les arguments en entrées comme cela. On se sert malgré tout de la structure d'un test unitaire pour faire nos premiers pas et avoir un bout de code qui tourne, dans un test.
* En analysant le code on se rends compte que le programme lit une certaine quantité d'entier. On essaye donc de les lui refiler et on arrive assez vite à quelques cas de tests qui couvrent les scenarios suivants: cas passant, cas impossbile, plusieurs cas (passant et/ou impossible). 
* On peut commencer a refactorer doucement le code en s'attaquant dans l'ordre:
 * A ce que l'IDE nous indique comme code mort
 * Travail en inlinant et en supprimant les variables inutiles
 * Travail sur la double boucle imbriqué et son test 'if' juste en dessous
 * Renommage des variables en des concepts plus parlant
 * Extraire les concepts en classes/structures pour répartir les comportements communs au même endroit et ajout de tests unitaires sur ces classes

Vous trouverez dans le repertoire [code](https://github.com/AxaWebCenter/Dojo-13/tree/master/code) des essais dans ce sens

A retenir sur ce kata :
* Dans le cadre d'un code hostile sans tests, des tests de bout en bout (end to end, boite noire etc...) nous permettent de découvrir le domaine et de comprendre le sujet. (Type technique Golden Master)
* Une fois le sujet compris et le harnais de tests en place, on peut refactorer paisiblement.
* On fait emerger un domaine métier qui se suffit à lui même en terme de documentation.
* Les tests bout en bout peuvent être remplacer/completer par des tests unitaires sur le comportement des nouveaux objets crées.





