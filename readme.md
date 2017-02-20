# Complete roguelike tutorial with libtcod and cl-tcod

## Introduction

This is a port of the Python code from the ["Complete Roguelike Tutorial, using python+libtcod"](http://www.roguebasin.com/index.php?title=Complete_Roguelike_Tutorial,_using_python%2Blibtcod) into Common Lisp using [cl-tcod](https://bitbucket.org/eeeickythump/cl-tcod). It uses [libtcod](https://bitbucket.org/libtcod/libtcod) (a.k.a. "The Doryen Library") through the Common Foreign Function Interface, [CFFI](https://common-lisp.net/project/cffi/). Commentary on writing this tutorial in lisp will be found on my [blog](https://9bladed.com).

The code is basically a straight "translation" from Python to Common Lisp, and is not necessarily "lispy" in it's current form. This was done on purpose to make it easy to refer to the original tutorial, and to reduce the chance of bugs in making sure this works as a proof of concept of a roguelike in lisp.

Everything works exactly the same in terms of gameplay and presentation, as near as I can tell. The only exception is that currently cannot restore savegames where a monster was confused (via a "scroll of confusion"). This is due to the use of a recursive anonymous function (lambda). There are probably several ways around this, but for the purposes of this tutorial translation this is a minor issue and will be left as is for now.

## Technical Details

cl-tcod is in the process of being updated to fix some bugs with the latest version of libtcod. Details here and on the blog posts will discuss the changes necessary if an updated version of cl-tcod is not on the official repository or mirrored on GitHub.

This code has only been tested with the current versions of libtcod (1.6.2), SBCL (1.3.12), and SDL (2.0.5) on x86_64 Arch Linux.

## Status

All of the code works (other than the saving caveat mentioned above), but is missing some of the original Python comments and lisp specific comments. The code is not necessarily pretty, well organized, or in a final state. Updates will be made as the blog posts go up for each part. It is possible in the future to produce a "lisp first" approach to the tutorial, but that is not planned yet.