## Coersion and Truthy/Falsey
### Type Coersion

Type conversion is exhibited when we try and equate 2 values to one another. Typically throughout the bootcamp so far we have been using '===' which checks if the 2 values are strict equals. This means that if the 2 values are not identical to one another it would return false as demonstrated below.
```javascript
23 === "23" // returns false
23 === 23 // returns true
```
'==' is the other comparative operator at our disposal which does not make sure that they are an identical match and uses type conversion to see if they technically equal one another. Unlike '===' which also checks if both values are the same data type, '==' will use a form of coersion to see if the values match.
```javascript
23 === "23" // returns true
```
The above statements are correct even in cases where we negate the comparative operator.

### Truthy and Falsey
Truthy and Falsey general terms which indicate whether a term is interpreted as true or false. Everything can be considered Truthy with exception to the following which are Falsey:
* False
* 0: the only falsey number
* "": an empty string is falsey
* null: an empty value is falsey
* undefined: an undefined object is considered falsey
* NaN: not a number is considered falsey

#### Using Truthy and Falsey
We can use Truthy and Falsey to quickly check true or false conditions in our code.
