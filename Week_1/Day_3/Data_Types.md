### Primitive Data Types
* undefined
* null
* boolean
* string
* number
* symbol - light weight strings
* big int - big ints are numbers too large to store in a number data type.

Trying to run a big int as a number can result in the loss of range or comparative ability inherent to numbers.

  ```javascript
  1....2 === 1....3 // => true
  ```
  In the example above assume that 1....2 and 1....3 are both big ints. But because they exceed the memory capacity of numbers javascript would consider them equals even though we clearly see that they are different numbers.