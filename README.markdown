Objector
========

_One who objects._

Objector is a Vim game to practice normal mode navigation, text-objects and, if
installed, the Surround plugin.

**Status:** Pre-Alpha, Design Phase

Outline
-------

* Randomly filled objects 'fall' from the top of the screen. These are created
  from a pool of object generators that have:
    * a presented pattern, e.g.: `"~"`
    * a target pattern, e.g.: `~`
    * a preferred solution, e.g.: `ds"`
* Every game-clock tick, the lines move down and a new top-most line (with a
  new object) appears.
* The line the cursor is on is not modified by the game engine. Lines above the
  cursor line will 'fall through' the cursor line (effectively skipping it and
  moving to the next line below the cursor).
* When the cursor lands on an object, its target object is printed in the line
  above it (temporarily overwriting any existing objects) (in a lighter
  colour?).
* When the current object matches its target object, the target is replaced
  with a score (in green?).
* The player's actual key-strokes are recorded for each objection.
* The number of characters typed by the player are compared to the number of
  characters in the 'preferred' solution and a base score is calculated based
  on the difference.
* If the player's actual key-strokes match the preferred solution, bonus points
  are awarded.
* The game ends when more than a `missLimit` number of objects 'fall' on the
  floor (the bottom-most line of the game area.)
* Total objections, key-strokes, time and accuracy are monitored and displayed
  either in the status bar or a 'status' line within the buffer.

