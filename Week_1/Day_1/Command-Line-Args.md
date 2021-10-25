### Command Line Arguments
[Command Line Arguments](https://stackabuse.com/command-line-arguments-in-node-js/) are way to call functions in a terminal with x amount of inputs declared in terminal.
### Format
The terminal will return the following:
* runtime: Location of the executable node version
* script_name: Name of the script that is being run
* argument: Arguments that were specified

### Example
```javascript
'use strict';

for (let j = 0; j < process.argv.length; j++) {
    console.log(j + ' -> ' + (process.argv[j]));
}
```
The code above is the function and typing "node processargv.js tom jack 43" into the terminal returns:

0 -> /home/vagrant/.nvm/versions/node/v12.22.7/bin/node

1 -> /vagrant/w1/d1-focal/processargv.js 

2 -> tom

3 -> jack

4 -> 43

### Assignment
We can assign the arguments we put in the terminal as an array like so:
```javascript
const args = process.argv.slice(2)
```
This returns the input arugments as an array called args and removes the location of node (0 in example above) and location of the script (1 in example above) we are running.