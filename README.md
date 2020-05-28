
# When John gambles at the casino, he always uses a special system of tactics that he devised himself. It's based on always betting in one of two ways in each game.
# codility gambles at the casino
# Wins in the casino are paid equal to the wager, so if he bets C chips and wins, he gets 2C chips back. If he loses, he doesn't get any chips back.

## Solution
```python
function solution(N, K) {
  let result = 0; // or: result = -1;
  while (N > 3 && K > 0) {
    if (N % 2) {
      N -= 1;
    } else {
      N /= 2;
      K -= 1;
    }
    result += 1;
  }
  return result + N - 1; // or: return result + N
}
```
console.log(solution(8, 0)); //7
console.log(solution(18, 2)); //6
console.log(solution(10, 10)); //4
