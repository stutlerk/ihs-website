---
layout: project
course: introcs

number: 4
title: Hangman
due: 2016-01-05
turnin: #
forum: #

rubric:
  total: 35
  behavior:
    criteria:
      - criterion:  Computer randomly chooses a secret word                                                                          
        value: 1 
      - criterion:  Host repeatedly asks for a letter and announces whether that letter is in the secret word                        
        value: 2 
      - criterion:  Assistant displays the correct secret word status after each guess                                               
        value: 4 
      - criterion:  Player loses a chance and a piece of the Hangman appears when a guess is incorrect                               
        value: 3 
      - criterion:  Host informs player when he or she guesses a letter that has already been guessed; player does not lose a chance 
        value: 3 
      - criterion:  Game ends with player victory if the entire secret word is guessed                                               
        value: 2 
      - criterion:  Game ends with player defeat if the player runs out of chances                                                   
        value: 2 
      - criterion:  Secret word is revealed when game ends                                                                           
        value: 2 
    total: 19 
  implementation:
    criteria:
      - criterion:  Program is well-designed visually and has a consistent theme                                                     
        value: 2
      - criterion:  Program is well-documented and exhibits good style                                                               
        value: 2 
      - criterion:  Program shows good creativity and effort                                                                         
        value: 3 
      - criterion:  Program uses custom blocks with arguments and reporters appropriately                                            
        value: 3
      - criterion:  Program includes at least two lists                                                                              
        value: 2 
      - criterion:  Program tracks guessed letters using a list                                                                      
        value: 2 
      - criterion:  Obtain and respond to playtest feedback from a parent or guardian                                                
        value: 2 
    total: 16 
---
### Overview

Hangman is a popular word game in which one player (the "chooser") chooses a secret word and another player (the "guesser") attempts to guess the word one letter at a time.  If a guessed letter appears in the word, all instances of it are revealed.  If not, the guesser loses a chance.  If the guesser figures out the secret word before he or she runs out of chances, he or she wins.  If not, the player who chose the word wins.  Traditionally, chances are tracked using a stick figure drawing of a person being hanged from a gallows.  The figure is drawn one body part at a time, and the guesser loses when the entire figure has been drawn. This game is also the basis for the TV game show Wheel of Fortune.

### Behavior

#### Gameplay
In our implementation of Hangman, the computer will take on the role of the "chooser" and the human player will be the "guesser."  The computer will secretly choose a word from a list (see below) and show the player how many letters are in the word by displaying a sequence of blanks (underscores).  Then, the computer will begin asking for guesses.  If the player guesses a letter that is in the secret word, all blanks representing an instance of that letter should be replaced by the letter.  If the guessed letter is not in the word at all, the player should lose a chance and a new part of the Hangman figure should appear.  If the player guesses a letter he or she has already guessed, he or she should not lose a chance, even if that letter is not in the word.  If the player guesses all letters in the word, he or she wins.  If the Hangman figure is completed, the player loses.  In either case, the secret word should be revealed after the game is over.

#### Sprites
Your game will need to include at least three sprites: the Hangman itself, a "host" sprite that asks the player for a guess and informs him or her whether or not the guess is correct, and an "assistant" sprite that tells the player the status of the secret word.  You may use more sprites if you think they are appropriate. The host and assistant should have clear roles and should never do each other's job.

#### Word Status
As the game is played, the player should be shown the current guessed status of the secret word.  Letters that have been correctly guessed should be shown in the correct locations.  Unguessed letters will appear as blanks.  At the beginning of the game, no letters will have been guessed, and the only information shown to the player will be a sequence of blanks, with one blank for each letter in the secret word.  As the player guesses letters correctly, blanks representing guessed letters should be replaced by those letters.  So, for example, if the secret word is "screwdriver" and the player has guessed 'e,' 's', 'r', and 'd,' the current word status would be "s _ r e _ d r _ _ e r".

#### Chances/The Hangman
The player will have six "chances" to guess the word.  Guessing a correct letter does not cost a chance.  Each missed chance will cause a new piece of the Hangman to appear.  The six pieces of the Hangman are: head, body, left arm, right arm, left leg, right leg.  You may use a stick figure for your Hangman, but if you would like to be more creative with the appearance, feel free to do so.  No matter what your hangman looks like, though, it should include these six pieces and no more.

#### Game End
The game can end in one of two ways:

* If the player has guessed the complete secret word, he or she wins.
* Otherwise, if the player has run out of chances and the complete Hangman has been drawn, the player loses.<br/>

In either case, when the game ends the host should stop asking for guesses.  The host should inform the player whether he or she won or lost, and the assistant should reveal the entire secret word.

### Implementation Details

#### Word List/Secret Word
You will be provided with a list of words from which the secret word should be chosen for each game.  You will be shown in class how to import this list into your program. At the start of each game, a word should be randomly chosen from this list to be used as the secret word.  The secret word must be chosen randomly, and must be a word in the list.

UPDATE: The word list is now available for download: []({{site.baseurl}}/introcs/wordsv2.txt)

#### Documentation
In addition to functioning well, your program must be well-documented and readable.  This includes, but is not limited to, things such as:

* organizing your scripts so that they can be read and comprehended easily
* giving  your sprites meaningful names
* naming and using your variables, lists, and custom blocks well
* including comments to describe the structure of your program and any particularly complex or unintuitive pieces of code

#### Required Snap! Elements
Your program must include, at a minimum, the following Snap! code elements:

* At least two lists, once of which must be used to track guessed letters
* Custom blocks as appropriate, including arguments and reporters

#### Parent Feedback
For this project, we will continue the process of undergoing a review of your work by an outsider reviewer.  This time, however, your program will be reviewed by a parent, guardian, or other adult family member.  After receiving your feedback, you should consider the comments carefully and respond.  You will turn in the feedback provided to you along with responses indicating how you modified your game in response to the feedback you received or why you chose not to make any changes.

Use the [Parent Feedback Form]({{site.baseurl}}/introcs/ParentFeedbackForm.docx) for all parent reviews.
