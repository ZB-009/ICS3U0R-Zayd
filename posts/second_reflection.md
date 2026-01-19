# Culminating Project 2026
## Learning Log 1
### January 11, 2026
#### For my Cookie Monster Runner game, I have decided to use at least 23 variables. 8 of these variables are used as coordinates for the player, robber, cookie, and traps, and are utilized in collision check methods and for moving the player. 4 other variables are used to initialize and save the size of each of these objects. Next, I am planning on using 5 boolean variables, 2 of which are used to start the game, 1 for changing the level, 1 to check if the game has been won, and the last variable for restarting the game. I also have variables that are used to switch between my backgrounds, increment score on collision with cookies, decrement score on collision with traps, and two timers, one to make the game more competitive, and another that is used to make text pop up on screen, then go off after a set time.

## Learning Log 2
### January 13, 2026
#### So far, I have used a lot of selection structures, including if-else statements and a switch case statement. The if statements have various uses, including checking if different boolean values are true or false, and running methods based on this information. For example, I have an if statement that is used to start the game. On mouseclicked between coordinates, the game will begin. I am also using a switch case to change between my backgrounds, which is also the first time I have used this function.

## Learning Log 3
### January 14, 2026
#### At the moment, I only have one repetition structure, which is used to create the values inside the rX and rY arrays, which will be used to draw the robber, cookies, and traps in later levels. I am planning on adding more repetition structures for other functions and methods, but I have not made a final decision on which functions yet.

## Learning Log 4
### January 17, 2026
#### I have 5 different arrays used for storing the values of the robber’s X and Y values, the cookie’s X and Y values, and to check if the different cookies are alive. The array, cookieAlive, that stores boolean values, is used first to store if a cookie exists or not, then check if there is a collision between the player and the cookie, making the value of cookieAlive[i] false.
#### void drawCookies() {
####  for (int i = 0; i<numCookies; i++) {
####    if (cookieAlive[i]) {
####      image(cookie, cookieX[i], cookieY[i], cSize, cSize);
####      if (cookieCollision(pX, pY, pSize, cookieX[i], cookieY[i], cSize)) {
####        cookieAlive[i] = false;
####      }
####    }
####  }
#### }
#### While attempting to remove cookies after they collided with the Cookie Monster, I ran into many issues actually removing them, and after trying a single boolean, which only made one of the three cookies disappear, I decided to make the variable an array, which worked and made all the cookies disappear on collision.

## Learning Log 5
### January 18, 2026
#### Throughout my code, I created many custom functions, most importantly of which are the various start game methods, the movement methods, and the methods that spawn the robber and cookies. 
| Method Name | void startGame()                             | void movePlayerRight()     | void robberLevel() |
|             |                                              | void movePlayerLeft()      | void drawCookies() |
|-------------|----------------------------------------------|----------------------------|:------------------:|
| Code Snippet| void startGame() {                           | void movePlayerRight() {   | void robberLevel() {
|             |    textSize(100);                            |  if (pX < width - pSize) { |   rSize = 100;
|             |   fill(255);                                 |    pX += pMove;            |   if (startDone && !cookiesPlaced) {
|             |   if (startButton) {                         |  }                         |     for (int i = 0; i < numCookies; i++) {
|             |     text("START", width/2-150, height/2);    | }                          |       cookieX[i] = rX[i+3];
|             |   }                                          |                            |       cookieY[i] = rY[i+3];
|             |   if (howButton) {                           | void movePlayerLeft() {    |       cookieAlive[i] = true;
|             |     fill(0);                                 |   if (pX > 0) {            |     }
|             |     rect(width-100, height-125, 75, 100, 10);|     pX -= pMove;           |     cookiesPlaced = true;
|             |     fill(255);                               |   }                        |     drawPlayer = true;
|             |     text("?", width-85, height-40);          | }                          |   }
|             |   }                                          |                            | }
|             |   if (!jarCollision) {                       |                            |
|             |     image(jar, jX, jY, jSize, jSize);        |                            | void drawCookies() { 
|             |   }                                          |                            |   
|             | }     `                                      |                            |
|             |                                              |                            |
|             |                                              |                            |
|             |                                              |                            |
|             |                                              |                            |
|             |                                              |                            |
|             |                                              |                            |
|             |                                              |
|             |                                              |
|             |                                              |
|             |                                              |
|             |                                              |
|             |
|             |
|             |
|             |
|             |
|             |
|             |
|             |
|             |
|             |
|             |
|             |
