# warsawJS Workshop#15: JavaScript basics with tic-tac-toe game

### Step 1
1. create `initGame()` function which:
    * gets all `<div>` elements inside `div.board` element
    * adds click event listener for each `<div>` with `fieldClickHandler` listener function

2. create `fieldClickHandler()` function which logs string 'Hello' and `this` to the console

### Step 2
1. inside `fieldClickHandler()` function add 'red' to clicked element classes (use native `classList.add()`)

### Step 3
1. at the top of the file:
    * declare `playerClasses` object to hold color for each player (playerA - 'red' and playerB - 'blue')
    * declare `currentPlayer` variable to hold currentPlayer name

2. inside fieldClickHandler()` function:
    * declare `playerClass` variable
    * assign to it name of the color of currentPlayer

### Step 4
1. remove click event listener from clicked element, so it is impossible to click one element twice (use `removeEventListener()` function)


### Step 5
1. at the top of the file declare `emptyFields` variable in which you will store number of empty fileds left
2. inside `initGame()` function assign to this variable number of empty fields at the beginning of the game (9)
3. inside `fieldClickHandler()` function:
    * decrease `emptyFields` variable by one
    * check if game has ended (game ends when emptyFields equals to 0)
    * if it has ended show alert on the screen (use built-in `alert()` function)

### Step 6
1. create new function `checkWinner()` and inside this function:
    * get all `<div>` elements inside `div.board` element and store it as a variable
    * think of possible winning scenarios for each player (how board looks like in horizontal, vertical and diagonal lines)
    * create string for each winning configuration, i.e. 'redredred' (use `fields[index].className` notation). Example: 
    ```js
    var row1 = fields[0].className + fields[1].className + fields[2].className;
    ```
    * use `if() {...}` statement to check if playerA or playerB has won the game
    * move end game check to the bottom of `checkWinner()` function

### Step 6a
1. create array with all winning configurations
2. change `if() {...}` statements to use `.includes()` to check the winner

### Step 7
1. reinitialize game once any of the players wins or there is no more empty fields on the board


### Step 7a 
1. to fix Chrome repainting bug use `setTimeout()` function for showing end of the game alert and reinitializing the game 