PedaBlackJack
Problem
Play the game with a standard deck of 52 cards. Make it so every time cards are dealt the exact cards are removed from the deck.
The exact cards dealt are removed but not deleted
There are 2 players: the house and the player. Create hand and card classes.
Inside of card class assign numerical (capable of math)
For this game Aces will only be worth 11 points as opposed to it being optional to represent 1 or 11.
When using switch and case define value of ace separately.
As cards are dealt we need to remove them from the playable deck so that cards are not duplicated during a round.
deck.Remove of some sort
Deal two cards to the house, hidden from the player until the house reveals its hand.
And let the player know the dealer has been dealt two cards (which have been removed from the deck but not deleted thus to allow the game to be played infinite times.
Deal two cards to the player that are both visible to the player.
And assign / check value of playerhand and dealerhand
Player plays first and is dealt 2 cards visible to the player.
Player has opportunity to hit or stand
Player can choose to stand with the cards they have, hit (dealt another) without exceeding 21 points at which point they bust.
Check value to make sure of values and add bust condition to while loop
If bust, game over.
Announce points and writeline who wins
If stand, dealer reveals cards and will hit if points <= 16 stand if score between 17 and 21 points. Results in bust if more than 21. Game over.

App should display winner. Winner is whichever player gets closet to 21 without going over therefor bust.

In the event of a tie the DEALER wins. If conditional where equal score || both bust, display DEALER wins.

Need to have the option of playing again which will start with a freshly shuffled deck of 52 cards.

Examples
The dealer has been dealt a 5 of spades and a queen of hearts. The player is dealt a 3 of clubs and a jack of hearts. The player's hand is displayed while the dealer’s not. The player goes first and hits, he draws an 8 of diamonds. He now has 21 points and will stand. The dealer then hits because he is under 17, draws a 4 of spades, and now has 21 points. In this scenario the players tie and the dealer wins.
The dealer has been dealt a 5 of spades and a queen of hearts. The player is dealt a 8 of clubs and a jack of hearts. The player's hand is displayed while the dealer’s not. The player goes first and hits, he draws an 8 of diamonds. He now has 18 points. The dealer then hits because he is under 17, draws a 4 of spades, and now has 19 points. The player stands (& display dealer cards) with 18 points and the dealer with 19. In this scenario the dealer wins.
The player is dealt a 10 of clubs and a jack of hearts. The dealer has been dealt a 6 of spades and a queen of hearts. The player’s hand is displayed while the dealer’s not. The player decides to stand(& display dealer cards to the player) because he has 20 points. The dealer has 16. In this scenario the player wins.
The dealer has been dealt a 10 of spades and a queen of hearts. The player is dealt a 2 of clubs and a jack of hearts. The player's hand is displayed while the dealer's hand is not. The player goes first and hits, he draws a 5 of diamonds. Because the dealer has over 17 points he will stand with 20 points (stand and display hand) In this scenario the dealer wins.
The dealer has been dealt a 5 of spades and a queen of hearts. . The player is dealt a 5 of clubs and a jack of hearts. The player's hand is displayed while the dealers’ not. The player goes first and hits, he draws an 8 of diamonds. He now has 23 which is a bust(over 21.) In this scenario the dealer wins.
The dealer has been dealt a 5 of spades and a queen of hearts. The player is dealt a 3 of clubs and a jack of hearts. The player's hand is displayed while the dealer is not. The player goes first and hits, he draws a 2 of spades. He now has 15. The dealer hits because he is under 17, he draws a 7 of spades which is a bust(over 21.) In this scenario the player wins.
Data structure
Card (class) Rank, Suit -value Deck = rank in ranks + “ of “ suit in suits -swapCards and randomNumberGenerator PlayerCards (class) top two cards [2][3] hit, add card -to playercards, stand -calculate value of playercards, bust -if value is over 21 player loses. WIN -value is greater than that of the dealer's hand (class) [0][1] (because dealt first) hit, add card -to dealer's hand, stand -calculate value of dealer's hand, bust -if value is over 21 dealer loses. WIN value is greater than that of the playercards
Algorithm 1 ) Create a full deck of 52 cards consisting of 2 properties dictating their suit and face. 2) Set the value of the cards to their corresponding integer value. 2 through 10 should equal the corresponding face value. Jack, Queen, and King of each suit should have a value of 10. Ace should be equal to 11. 3) Set parameters for playerHand. When the sum of total value of cards in playerHand is less than or equal to 21, ask the player if they would like to hit (dealt another card) or stand (continue with the value of the cards already dealt in their hand). If playHand is greater than 21 then it results in bust (exceeds point allowance) and the dealer wins. 4) Set parameters for dealer Hand. When the sum of total value of cards in dealer Hand is less than or equal to 16 ask the player if they would like to hit (dealt another card) or stand (continue with the value of the cards already dealt in their hand). If dealerHand value is 17 to 21 then make the dealer stand. If dealerHand is greater than 21 then it results in bust (exceeds point allowance) and the player wins. If the end result is a tie dealer wins. 5) Randomly shuffle the deck of 52 cards. 6) Deal 2 cards to playerHand that are visible to the player.
Deal 2 cards to dealer Hand that are hidden from player view until player elects to stand. 8) Display sum of playerHand and ask player if they want to hit or stand. 9) If player elects hit ask again until player selects stand or bust occurs.
10 Sum should be updated to include the total value of each card player has been dealt and the same for the dealer hand. 11) If the player selects stand before the bust occurs then reveal dealerHand. 12) Display sum of dealerHand and ask dealer if they want to hit or stand. 13) If hit, dealer is dealt card and ask again. 14) If dealerHand less than 17 hit and continue asking until sum of Dealerhand is greater than or equal to 17. If greater than or equal to seventeen dealer will stand. If greater than 21 results in a bust, the player wins.
15 If both players select to stand during this process, compare the values of each player's hand and determine the match result. If houseHand is greater than or equal to the value of playerHand, house wins. If playerHand is greater than houseHand, player wins.
16 Once a winner is declared, prompt to play again starts from step 5 with the same settings we established in steps 1-4.
