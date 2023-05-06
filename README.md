Download Link: https://assignmentchef.com/product/solved-eecs-1015-lab-4-functions
<br>






<ol start="2">

 <li><strong>LAB 4 – TASK/INSTRUCTIONS </strong></li>

</ol>

<strong>Task 0: [This will be the same for all labs]: </strong>Start you code with comments that include this lab ID, your full name, email address, and student id as follows:

<strong># Lab 4 </strong>

<strong># Author: Michael S. Brown </strong>

<strong># Email: <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="ddb0aebfe4e4e5e4e59dbcb2b1f3beb2b0">[email protected]</a> # Student ID: 10233030 </strong>

<strong> </strong>

<strong>This lab has only 1 task.  Please read carefully.  A video of this lab running is available here. </strong>

<a href="https://www.eecs.yorku.ca/~mbrown/EECS1015_Lab4.mp4"><strong>https://www.eecs.yorku.ca/~mbrown/EECS1015_Lab4.mp4</strong></a> <strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>See explanation of the task on next page. </strong>

<strong>          </strong>

<strong>Main Task – Two Card Poker Game </strong>

In this lab you are to write a simple two card poker game as follows:

Each play of the game, the <strong>user</strong> will get two cards and the <strong>computer</strong> will get two cards.

Cards are an integer value between 2-14, but are printed out as 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A The winner of the game is based on the following rankings:

<em>Pair (2 cards of the same value) </em>

<ul>

 <li><em>if both players have a pair, then the pair with the highest numerical value wins </em></li>

 <li><em>if only one player has a pair, then the pair wins </em></li>

</ul>

<em>Highest Cards </em>

<ul>

 <li><em>if neither player has a pair, then the player with the highest card wins. </em></li>

 <li><em>if both players highest card is the same, then the winner goes to the player with the second highest card Tie: If both players have the exact same cards then no winner, it is a tie </em></li>

</ul>

<strong>Example</strong>:

[A] [A] beats [K] [K]  — when both players have a pair, the highest pair wins

[2] [2] beats [A] [K]  — if only one player has a pair, the pair wins

[A] [K] beats [A] [Q] – if neither has a pair, the highest card wins.  If both players have the same highest card, then the                                         2<sup>nd</sup> highest card wins (in this case, [K] (13) beats [Q] (12) ) [A] [2] beats [K] [Q] – Otherwise, the highest card wins.

If both plays have the same card, then it is a tie (e.g., [J] [8] and [J] [8] is a tie)

<strong>Your requirements – read carefully, there are functions you must define to get full marks: </strong>

<ul>

 <li>Write a function named drawcards() [no parameters] that generates <strong>two</strong> random cards represented as integers with values [2 to 14] inclusive. Your function should return the two cards such that the first card is greater than or equal to the second card.</li>

</ul>

For example, if random numbers are 2 and 13, then your function should return in the order 13 and 2.

<em>Please see notes on how to return two values with a function. </em>

<em> </em>

<ul>

 <li>Write a function named card2str() [one parameter] that will convert a card integer value to a string and return the string result. Use the following conversion:</li>

</ul>

Cards with values between 2-10 should be converted their string representation “2” – “10”.

Card value 11 is “J”, value 12 is “Q”, value 13 is “K” and value 14 is “A”.

For example, card2str(2) will return “2”.  card2str(12) will return “Q”




<ul>

 <li>Write a function named printhand() [three parameters] that will print out the two cards as follows (depending on the player and their cards). [A] [2] Your Cards</li>

</ul>

[3] [3] Computer’s Cards




<ul>

 <li>Write a function named printoutcome() [four parameters] that will print out if you win, lose, or tie. This function should take four arguments (your 2 cards and the computer’s 2 cards).  In my opinion, this is the most difficult function for lab 4.  Take care to get it work properly.  This functoin needs to compute the correct answer based on the ranking criteria above.</li>

 <li>You program should play one round of the game an then ask the user if you’d like to play again (Y/N). If the user doesn’t type in “N” or “n”, keep playing the game.</li>

</ul>




Note that you can have more functions that mentioned above, but we will be expecting to see: drawCards, card2str, printhand, printoutput




<em>See next page for example game play. </em>

Example of game play:

** EECS1015 — AMAZING TWO CARD POKER GAME **

<table width="126">

 <tbody>

  <tr>

   <td width="126">Pair wins</td>

  </tr>

 </tbody>

</table>

[K] [K] YOUR CARDS

[K] [9] COMPUTER’S CARDS

YOU WIN

Want to play again? (Y/N) y

<table width="126">

 <tbody>

  <tr>

   <td width="126">High card wins</td>

  </tr>

 </tbody>

</table>

[10] [9] YOUR CARDS

[9] [7] COMPUTER’S CARDS

YOU WIN

Want to play again? (Y/N) y

<table width="126">

 <tbody>

  <tr>

   <td width="126">High card wins</td>

  </tr>

 </tbody>

</table>

[K] [9] YOUR CARDS

[Q] [5] COMPUTER’S CARDS

YOU WIN

Want to play again? (Y/N) y

[7] [7] YOUR CARDS              Highest pair wins

[A] [A] COMPUTER’S CARDS  YOU LOSE!

Want to play again? (Y/N) y

[7] [4] YOUR CARDS              High card wins

[10] [4] COMPUTER’S CARDS

YOU LOSE

Want to play again? (Y/N) y

[J] [9] YOUR CARDS              High card wins

[6] [5] COMPUTER’S CARDS

YOU WIN

Want to play again? (Y/N) y

[A] [2] YOUR CARDS               High card wins

[Q] [8] COMPUTER’S CARDS

YOU WIN

Want to play again? (Y/N) y

[J] [10] YOUR CARDS             High card wins

[Q] [2] COMPUTER’S CARDS

YOU LOSE

Want to play again? (Y/N) y

[7] [6] YOUR CARDS              High card wins

[9] [7] COMPUTER’S CARDS

YOU LOSE

Want to play again? (Y/N) y

[A] [9] YOUR CARDS              2<sup>nd</sup> highest card wins

[A] [2] COMPUTER’S CARDS

YOU WIN

Want to play again? (Y/N) y

[J] [8] YOUR CARDS               High card wins

[Q] [2] COMPUTER’S CARDS

YOU LOSE

Want to play again? (Y/N) N      STOP PLAYING<sup>                     </sup>

** Thank you for playing! **

















