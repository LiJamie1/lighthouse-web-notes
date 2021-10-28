## Objects
Objects are not a primitive data type. As it references and stores other forms of data.

### In an Object:
* There are key value pairs: each key maps to a value
* Keys are always in the form of strings
* There cannot contain 2 keys with the same name
* Any valid javascript value can be stored (other objects, functions or primitive data types.)

### Keys are:
* Always Strings
* Unique
* Associated with **ONE VALUE**

Object Literals: These are objects that we specifically with predefined keys and values. It quite literally refers to the value of the object, in the case below everything withing the {} is the Object literal.

```javascript
const bakeryInventory = {
  cakes: 10
  cookies: 5
  bread: 2
}
```
The key in this case does not need to be encased in '' as it is by default recognised as a string by javascript when calling the object or specific key.

Objects can be seen as 2 column tables, on one side we have the key associated and on the other we have the value that is tied to the key.
The object:
```javascript
const object = {
  name: "Jamie",
  age: 23,
  gender: "Male"
}
```
could be visualised as the table below:
| Key     | Value      |
| ------ |:--------:|
| name    | Jamie |
| age    | 23     |
| gender | Male      |

When calling a specific key we tend to use [] notation and place nest the key in ''s like so ['name']. Not nesting the key in quotes will make javascript look for a variable called name in the object as opposed to the key.

Furthermore, [] notation can be used to add more key value pairs as shown below:
```javascript
object["address"] = {
  "street":  "foo",
  "city": "Vancouver",
  "postalCode": "bar"
}

=>

const object = {
  name: "Jamie",
  age: 23,
  gender: "Male",
  adress: {
    "street":  "foo",
    "city": "Vancouver",
    "postalCode": "bar"
  }
}
```

As mentioned previously and shown above Object values can be any valid javascript value. As such we can nest an object in side an object.

### Iterating Through Objects
Objects themselves are not iterable as the keys are strings unlike in arrays where the indexes are numbers which are easy to iterate witha for loop.

Object.keys(...) is a way to inspect and iterate through an object keys. This will identify the keys and allow us to see what information is stored in said object.

Or we could use for...in to iterate through an object. For in would return to us each key in an object. For example:
```javascript
const planetMoons = {
  mercury: 0,
  venus: 0,
  earth: 1,
  mars: 2,
  jupiter: 67,
  saturn: 62,
  uranus: 27,
  neptune: 14
};

for (var planet in planetMoons) {
  var numberOfMoons = planetMoons[planet];
  console.log("Planet: " + planet + ", # of Moons: "+ numberOfMoons);
}
```

The object above has 8 keys and the for in loop will cycle through them. By creating a variable called planet and temporarily giving the directory of each key to planet, we will get a console message for every loop completed. For instance the key "earth" with a value of 2 would return in console "Planet: earth, # of Moons: 1"

For...in has limitations in that it can produce unexpected results and sometimes require an additional step to filter the object to avoid these errors.
