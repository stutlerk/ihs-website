---
layout: project
course: introcs

number: 3
title: Pong
due: 2015-12-07
turnin: https://canvas.instructure.com/courses/974357/assignments/4105679
forum: #

checkpoints: 
  - title: Checkpoint 1 - Fundamentals
    date: 2015-11-24
    value: 10%
    description: Players can control paddles; the ball starts in the middle, moves in a random direction, and bounces of edges of stage
  - title: Checkpoint 2 - Ball Movement
    date: 2015-12-01
    value: 10%
    description: The ball bounces and speeds up when it hits a paddle, and resets to the middle and scores a point when it hits the left or right edge

rubric:
  total: 40
  behavior:
    criteria:
      - criterion:  Players can control paddles with required keys                                       
        value: 2   
      - criterion:  Ball begins play at middle of field at start of game and after each point            
        value: 3   
      - criterion:  Ball bounces correctly off upper and lower edges and paddles                         
        value: 3   
      - criterion:  Ball increases in speed each time it bounces off a paddle                            
        value: 3
      - criterion:  Each player's score is displayed
        value: 1
      - criterion:  A point is scored for the opponent each time the ball touches the left or right edge 
        value: 2   
      - criterion:  Game ends when one player reaches five points                                        
        value: 2   
      - criterion:  Winning player is shown when game ends                                               
        value: 1    
      - criterion:  Players can begin a new game                                                         
        value: 1    
    total: 18
  implementation:
    criteria:
      - criterion:  Gameplay is smooth, polished, and intuitive                                          
        value: 2   
      - criterion:  Program shows good creativity and effort                                             
        value: 2   
      - criterion:  Program is well-documented and exhibits good style                                   
        value: 2   
      - criterion:  Program includes at least three custom blocks, including at least one with arguments 
        value: 3   
      - criterion:  Additional custom blocks, including arguments and reporters, are used where appropriate         
        value: 1   
      - criterion:  Provide valuable playtest feedback to at least two other students
        value: 2
      - criterion:  Obtain and respond to playtest feedback from at least two other students
        value: 2        
      - criterion:  Checkpoint 1                                                                         
        value: 4   
      - criterion:  Checkpoint 2                                                                         
        value: 4    
    total: 22
---
### Overview

In 1972, when video games were still very new and relatively unknown, a new game took the world by storm.  A simple simulation of tennis using two-dimensional graphics, minimal sounds, and extremely basic controls, Pong became the first arcade game to achieve widespread popularity and is credited as the genesis of the modern video game industry.  Today, the game has been played, remade, spun-off, and referenced innumerable times and it remains, to many, the single most identifiable and recognizable game in the history of video games.

### Behavior

####  Gameplay
Pong is played by two players each controlling a paddle with the goal of defending their end of the "field."  A ball begins play in the middle of the screen and, at the start of each round, moves in a random direction.  The ball bounces off the upper and lower edges of the field and the players' paddles.  Each time the ball bounces off a paddle, its speed increases by a small amount.  When the ball bounces off a paddle, its direction is reversed with a small random variation to add unpredictability to the game.

####  Scoring
Each player has a score, which should be displayed on the stage.  If the ball touches the left or right edge of the field, a point is scored for the opponent of the player who was defending that edge and the ball resets to the middle of the field.  When one player reaches 5 points, the game is over and that player is the winner.  The winner is announced on the screen and the players are given the opportunity to start a new game.

#### Player Control
Paddles are positioned a short distance away from the side they are defending, and can only move up and down, not side to side.  Each player should have two keys to control the movement of their paddle: one for up, and one for down.  Paddles move at a set speed that is the same for both players can cannot be controlled.  The player on the left will control his/her paddle with the 'w' and 's' keys.  The player on the right will use the up arrow and down arrow keys.
        
### Implementation Details

#### Custom Blocks
Throughout your program, you should use custom blocks to generalize common operations and increase the readability and maintainability of your code.  Your program must include at least three custom blocks, at least one of which must take arguments.  Do not limit yourself to just three blocks: use custom blocks (including arguments and reporters) anywhere you feel it will help your code.  Part of your grade will be based on not only meeting the minimum usage requirement but also on your decisions of when, where, and how to use custom blocks.

#### Documentation
In addition to functioning well, your program must be well-documented and readable.  This includes, but is not limited to, things such as:

* organizing your scripts so that they can be read and comprehended easily
* giving your sprites meaningful names
* naming and using your variables well
* naming custom blocks and arguments well
* including comments to describe the structure of your program and any particularly complex or unintuitive pieces of code

#### Peer Feedback
As part of the software development experience on this project, you will participate in a peer review with one or more of your classmates.  Near the end of the project, you will play other students' game and provide them with notes and comments.  Your partners will also play your game and offer the same feedback.  You should offer suggestions for features that could be improved or changed as well as look for bugs in the program you are reviewing.  Keep your comments constructive and professional!  Don't just point out things you don't like— explain your thinking and propose solutions.  Also, restrict your comments to things that can be reasonably addressed.  Do not tell your partner that he or she made a poor choice of theme and should start over, for example.

After receiving your peer feedback, you should consider the comments carefully and respond.  You will turn in the feedback provided to you along with responses indicating how you modified your game in response to the feedback you received or why you chose not to make any changes.

Use the [Peer Feedback Form]({{site.baseurl}}/introcs/PeerFeedbackForm.docx) for all peer reviews.  Both the reviewer and the developer will submit the form, so make sure you share the completed form with each other.
