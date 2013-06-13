---
title: Typography Testing  
layout: post  
published: false  
tags: [code]  
---

Lately I've been watching an iTunes U computer science course; [CS50 from Harvard University][cs50]. Not only is [David J. Malan][david malan] an excellent lecturer, but it's free! Thank you internet. Anyway, as part of the course, one of the exercises set was to solve the [game of fifteen][puzzle15 wikipedia] so I decided to have a crack at writing a solver in javascript.

The result can be found here <http://15puzzle.dalrimple.com>. It's a single page of html, css and javascript. Check out the [github repo][github repo] for fully annotated code.

##Breaking down the problem
For starters I didn't know how to solve the puzzle by hand, let alone by code. So I downloaded a game of fifteen [app][sliderpuzzle app] onto my phone and played it until I worked out a repeatable method for solving the board. The solution I ended up with was to break the board into 4 corners, each with their own method for completion.

###Top Left
The top left region contains all tiles excluding the two right most columns and two bottom most rows. Moving tiles into position in this section of the board is relatively easy. 

1. Identify the next tile to be solved in this region.
2. Map a path between where the tile is, and where the tile belongs. Make sure to avoid any tiles that are already solved.
3. Map a path between where the blank space is and the next step of the path mapped in step 2. Make sure to avoid any tiles that are already solved and the tile you are trying to move.
4. Once the blank space has reached the next step of the tile's path, move the tile one step along it's path.
5. Repeat steps 3 and 4 until the tile has reached it's destination.
6. Go back to step 1 for the next tile to be solved.

####Top Right
The top right region contains all the tile in the two right most columns excluding the bottom 4. Moving tiles into position here is a bit trickier. They have to be moved in pairs otherwise you end up with an incorrect tile stuck in a space where the correct tile should go.

1. Identify the next two tiles that sit at the top of the two columns
2. Whichever is closest, map a path to the position next to where it belongs. Make sure to avoid any tiles that are already solved and the tile you are trying to move
3. Repeat step 2 for the furthest except that it needs to sit underneath the tile that has just been moved.
4. Move the blank space next to the first tile
5. Move the first tile into its destination
6. Move the second tile into its destination
7. Go back to step 1 for the next pair of tiles to be solved.

One thing to watch out for is that if both the tiles to be solved are close to their destinations, it may not be possible to solve them with the steps above. To get around this, move the furthest tile to be at least 2 rows away from it's destination before step 2.

#####Bottom Left
The bottom left region is equivalent to the top right; all the tiles in the bottom two rows excluding the four to the right. Similarly tiles need to be moved into position in pairs. It's a little more complex here because the pairs are not consecutive. The first pair would be made up of the first tile in the top row plus the first tile in the the bottom row.

Follow the same steps as for the top right region but instead of moving top down, run the steps left to right.

######Bottom Right
Lastly, the remaining 3 tiles to be solved will be in the four spaces that are left. Funnily enough you can follow exactly the same steps for the top left to solve this region.

<!--Link references-->
[cs50]: http://cs50.tv/2011/fall/ "Harvard CS50"
[david malan]: http://cs.harvard.edu/malan/ "David J. Malan"
[puzzle15 wikipedia]: http://en.wikipedia.org/wiki/15_puzzle "Game of 15 Wikipedia Page"
[sliderpuzzle app]: https://itunes.apple.com/au/app/slide.puzzle/id517511112?mt=8 "Slider Puzzle iPhone app"
[github repo]: https://github.com/dalrimple/15puzzle "15 Puzzle Github repo"
[contact]: /contact "Contact Page"