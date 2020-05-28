
When John gambles at the casino, he always uses a special system of tactics that he devised himself. It's based on always betting in one of two ways in each game.
codility gambles at the casino
Wins in the casino are paid equal to the wager, so if he bets C chips and wins, he gets 2C chips back. If he loses, he doesn't get any chips back.

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

ref: https://stackoverflow.com/questions/58055310/how-can-i-break-down-this-gambling-problem



given S = "1111010101111" the function should return 22
string S of length N which encodes a non-negative number V in a binary form 3 given S = "1111010101111" the function should return 22.

## Solution
```python
function solution(N, K) {
  var num = 0, p = 1;
	for(var i=S.length - 1;i>=0;i--) {
		num += S.charAt(i) == '1' ? p : 0;
		p*=2;
	}
	var res = 0;
	while(num > 0) {
		if(num%2 == 0)
			num/=2;
		else
			num--;
		res++;
	}
	return res;
}
```

ref: https://leetcode.com/discuss/interview-question/651142/Microsoft-Online-Assesment-Question


