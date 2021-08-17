# Rock Paper Scissors Game

### Introduction

We're going to make a simple implementation of grade-school classic "rock paper scissors".  If you don't know what that is check the [Wikipedia article](https://en.wikipedia.org/wiki/Rock%E2%80%93paper%E2%80%93scissors) or [this](https://www.wikihow.com/Play-Rock,-Paper,-Scissors) ridiculous step-by-step.  For the moment we're just going to play the game from the browser console, but we will revisit it and add a front end later so don't forget to keep the code on GitHub! You might notice some 'view in browser' links in the student solutions - this is coming in a later lesson.  When you get there don't forget to come back and add  your link!

### Assignment 1

<div class="lesson-content__panel" markdown="1">
1. Start a new Git repo for your project.
2. Create a blank HTML document with a script tag.  This game is going to be played
    completely from the console, so don't worry about putting anything else in there.
3. Your game is going to play against the computer, so begin with a function called `computerPlay` that will randomly return either 'Rock', 'Paper' or 'Scissors'.  We'll use this function in the game to make the computer's play.
4. Write a function that plays a single round of Rock Paper Scissors.  The function should take two parameters - the `playerSelection` and `computerSelection` - and then return a string that declares the winner of the round like so: `"You Lose! Paper beats Rock"`
   1. Make your function case insensitive (so users can input `rock`, `ROCK`, `RocK` or any other variation)

   2. __Important note:__ you want to `return` the results of this function call, _not_ `console.log()` them.  To test this function console.log the results:

      ~~~javascript
      function playRound(playerSelection, computerSelection) {
      	// your code here!
      }

      const playerSelection = 'rock'
      const computerSelection = computerPlay()
      console.log(playRound(playerSelection, computerSelection))
      ~~~


5. Write a NEW function called `game()`. Use the previous function _inside_ of this one to play a 5 round game that keeps score and reports a winner or loser at the end.
   1. You have not officially learned how to "loop" over code to repeat function calls... if you already know about loops from somewhere else (or if you feel like doing some more learning) feel free to use them.  If not, don't worry! Just call your `playRound` function 5 times in a row.  Loops are covered in the next lesson.
   1. At this point you should be using `console.log()` to display the results of each round and the winner at the end.
   2. Use `prompt()` to get input from the user. [Read the docs here if you need to.](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt)
   3. Feel free to re-work your previous functions if you need to.  Specifically, you might want to change the return value to something more useful.
   4. Feel free to create more "helper" functions if you think it would be useful.

</div>

### Assignment 2

Go back to your “Rock Paper Scissors” game from a previous lesson and give it a simple UI so that the player can play the game by clicking on buttons rather than typing their answer in a prompt.
1. Copy your original code into a new file so you don’t lose it.
    - _Stored in the "console" branch of this project_
    
2. For now, remove the logic that plays exactly five rounds.
3. Create three buttons, one for each selection. Add an event listener to the buttons that calls your `playRound` function with the correct `playerSelection` every time a button is clicked. (you can keep the console.logs for this step)
4. Add a `div` for displaying results and change all of your `console.logs` into DOM methods.
5. Display the running score, and announce a winner of the game once one player reaches 5 points.
6. You will likely have to refactor (rework/rewrite) your original code to make it work for this. That’s OK! Reworking old code is an important part of the programmer’s life.
7. Don’t forget to go back and add your new version to the original Rock Paper Scissors Project!
