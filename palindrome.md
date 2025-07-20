

# Approach
1. duplicate original number
2. initialize reverse = 0
3. iterate and find the reverse
4. check if there is reverse == original number
5. return `true` otherwise `false`


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
