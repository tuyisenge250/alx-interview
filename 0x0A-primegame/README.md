isWinner Function
Overview
The isWinner function determines the winner of a series of rounds in a game played between two players, Maria and Ben. The game is played with a set of consecutive integers starting from 1 up to and including n. Players take turns choosing a prime number from the set, removing that number and all its multiples from the set. Maria always goes first, and both players play optimally. The player who cannot make a move loses the game.

Function Prototype
python
Copy code
def isWinner(x, nums):
Parameters
x (int): The number of rounds to be played.
nums (list of int): An array containing the values of n for each round.
Returns
str: The name of the player who won the most rounds, either "Maria" or "Ben".
None: If there is no clear winner (i.e., both players win the same number of rounds).
Example
python
Copy code
x = 3
nums = [4, 5, 1]
result = isWinner(x, nums)
print(result)  # Output: "Maria"
Explanation of Example
First round (n=4): Maria picks 2, removing 2 and 4. Ben picks 3, removing 3. Ben wins as Maria cannot make a move.
Second round (n=5): Maria picks 2, removing 2 and 4. Ben picks 3, removing 3. Maria picks 5 and wins.
Third round (n=1): Ben wins automatically as there are no primes for Maria to pick.
Maria wins 2 out of 3 rounds, so the function returns "Maria".

Assumptions
n and x will not exceed 10,000.
The function does not import any external packages.
Optimal Strategy
Both players play optimally, meaning they always make the move that maximizes their chances of winning.

How It Works
Prime Number Selection: The function determines the prime numbers within the range [1, n].
Game Simulation: The function simulates the game for each value of n, tracking the winner for each round.
Result Calculation: After all rounds are played, the function counts the wins for Maria and Ben, returning the name of the player with the most wins or None if there’s a tie.
Edge Cases
If n = 1, Ben automatically wins as there are no prime numbers to choose.
If both players win the same number of rounds, the function returns None.