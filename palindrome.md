

# Approach
<!-- Describe your approach to solving the problem. -->

# Complexity
- Time complexity:
O(Log(N))



# Code
```javascript []
/**
 * @param {number} x
 * @return {boolean}
 */
var isPalindrome = function(x) {
    
 duplicateNumber = x;
  if (x < 0) {
    return false;
  }

  if (x == 0) {
    return true;
  }

  let reverse = 0;
  while (duplicateNumber > 0) {
    let lastDigit = duplicateNumber % 10;
    duplicateNumber = Math.floor(duplicateNumber / 10);

    reverse = reverse * 10 + lastDigit;
  }

  return reverse === x;

};
```
