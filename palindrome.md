

# Approach
<!-- Describe your approach to solving the problem. -->
1. Duplicate the number
2. INitialize reverse = 0
3. Iterate over duplicate number to find reverse of a number
4. Check `original == reverse number`
5. return `true` or `false`
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
