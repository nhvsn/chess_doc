# Chess Board

create a class for the Game

the class will have a constructor property for each piece

    Each piece will then have properties:
      1) access to the board
      2) access to each square
      3) color
      4) allowed moves
      5) blocked moves
      6) css/html attributes

    The board will have functionality:
      1) what happens when a player clicks on the piece
      2) what happens when a player is dragging? the piece
      3) what happens when a player drops/unclicks from a piece

---

    Moving a piece:
      1) depending on which piece the player clicks on on the board..
        A) first we will need to keep track of the piece that the player actually clicks on:

    Moves available of pieces:
      1) we will need a list of pieces for each team
      2) we will need a list of positions of pieces for each team
      3) if piece is being moved
        A) BlockedPosition
          a) if blockedPosition is within AllowedMove list, the move is an attack/take move, takepiece, it will then do a check/checkmate call to see whether AFTER this move, it is a check or checkmate
          b) if it's blocked and is own color, disallow
        B) UnblockedPosition
          a) once the piece is clicked and dropped to a cell and within the AllowedMove list, move the piece
          b) if its not within the list, disallow

    CheckKing:
      1) this function will check whether after a move has been made is a check to the other teams King

    CheckmateKing:
      1) this function will check whether after a move has been made is a checkmate to the other teams King, this will end game

    TakePiece:
      1) function will remove the opponents team piece,
        a) could add some functionality where it shows what pieces the current team has taken from opponent
      2) Clear the square after taking piece

    AllowedMoves:
      1) each piece (depending on the class: Bishop, Pawn, Rook, etc) when clicked on will have a list of allowed moves/positions

    Change the turn:
      1) once a piece has been moved, if the team that moved it was white, change it to black and vice versa

## Pawns

class Pawn will have a constructor in which the parameter consists of position and name
-position will define where it lies on the board
-name will define the team/color of the piece and number as well (eg. each team has 9 Pawns)

within the class Pawn,
it will have a function that tells what kind of moves the Pawn can make
-Allowed moves will depend on the position (eg.meaning if it hasn't moved from original position, it can move UP to 2 spaces forward, otherwise, one space)
-Attacking/Take move will only consist of a diagonal move going forward from its position
-have a function to change its position

## Rooks

## Bishop

## Knight

## Queen

## King
