# AIT YAHIA Maya 

## Exercices

Cette semaine, j'ai regardé les vidéos du MOOC sur le double dispatch, un concept qui permet de choisir la méthode appropriée en fonction de deux objets. Contrairement au simple dispatch, où la méthode est déterminée uniquement en fonction du receveur du message, le double dispatch prend en compte à la fois le receveur et l'argument, ce qui améliore la flexibilité du code.

Pour mettre ce concept en pratique, j'ai implémenté DSLDoubleDispatch et PaperStoneScissor.  Ils sont accessibles sur GitHub aux liens suivants :
https://github.com/aityahiaM/DSLDoubleDispatch
https://github.com/aityahiaM/PaperStoneScissor


En réalisant ces exercices, j'ai constaté que le double dispatch rend le code plus lisible et modulaire, tout en facilitant l'ajout de nouveaux éléments sans avoir besoin de modifier les classes existantes.

## Mon kata : 

Cette semaine, j'ai réussi à corriger le déplacement des pions en diagonale pour capturer d'autres pièces. Cependant, il me reste à gérer le mouvement "En passant". 

# COUNDOUL Adama

## Exercices 

Essence of dispatch is :
-Do not ask tell 
-Let the receiver decide.

To practice the double dispatch , I work on implementing the double dispatch on the die/dieHandle excercise.

Here is the code : https://github.com/adama-coundoul/MyCounter

## Chess Game 
In my Pharo chess game, I am working on the pawn promotion feature. When a pawn reaches the last row of the board (8th for white, 1st for black), it needs to be promoted to another piece (queen, rook, knight, or bishop).

### Two Game Modes
There are two modes in the game:
Automatic Mode: This is when the player clicks the "Play" button. The game runs automatically, and in this case, I decided to always promote the pawn to a queen for simplicity.
Interactive Mode: This is when the player clicks on a pawn directly to move it. In this mode, the player should be able to choose the piece for the promotion.

### What I Have Done

For automatic mode, I added a method moveToAutomaticVersion: that handles the move and automatically promotes the pawn to a queen when it reaches the last row. i call it in the play method.
For interactive mode, I have not yet implemented the choice part. My plan is to detect when the game is in interactive mode , and then show a dialog box asking the player to pick the piece for promotion.
I found the classes MySelectedState and MyUnselectedState, which define methods like clickOn: aMyChessSquare. So, I think these methods operate on the chess square itself, not directly on the pawn.

```
clickOn: aMyChessSquare
	"We should only move if it's legal but..."

	selection unselect.
	selection contents ifNotNil: [
		board unhighLightTargets: selection contents targetSquares.
		board game move: selection contents to: aMyChessSquare ].

	^ MyUnselectedState board: board
```
I understand with this method that "selection contents" return the piece selected . I will just change this method moveTo to moveToInteractiverVersion.

### Next Steps
Finish the moveToInteractiveVersion: method to manage the player choice .


