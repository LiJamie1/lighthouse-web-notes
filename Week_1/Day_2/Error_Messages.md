### Error Messages

Error messages are important and very helpful in finding out where your code went wrong. At first glance the error message below can seem confusing but breaking it down can show us where the errors are in our code.
```
node syntax-error.js
/vagrant/w1d2/syntax-error.js:4
console.log(rank name);
                 ^^^^
SyntaxError: Unexpected identifier
    at exports.runInThisContext (vm.js:73:16)
    at Module._compile (module.js:443:25)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
```
### The first line can exhibit various types of errors:
* Syntax errors: misplacing/forgetting a closing bracket
* Reference errors: misspelling a variable in a function call
* Type errors: ie a method not applying to a data type

#### The **first line** of the error below indicates which file the error occured in. In this case 
```
/vagrant/w1d2/syntax-error.js:4
```
caused the error. This references that line 4 in syntax-error.js has a problem.

#### The **second, third and fourth line** 
```
console.log(rank name);
                 ^^^^
SyntaxError: Unexpected identifier
```
shows exactly where the error occured on line 4. In the case above the error came from the identifier "name".

#### The last section of the error message is a ***Stack Trace***
```
 at exports.runInThisContext (vm.js:73:16)
    at Module._compile (module.js:443:25)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
```
This shows the state of our program when the error occured. We will learn about these at a later date in the bootcamp.

### Debugging

A common tool to use is console.log as we can place it in various places in our code and watch how the input or data changes as the script runs. This mainly helps with figuring out why your function or script is printing out the wrong values.