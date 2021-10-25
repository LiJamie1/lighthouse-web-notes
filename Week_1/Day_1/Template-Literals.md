### Concatenation vs Interpolation
Concatenation is the combination of strings and variables with the + operator:
```javascript
let name = Jamie
"Hello " + name + "!"
```

Interpolation is a template where the variables are placed in the string without the need of the + operator and the need to break up the string. It instead uses back ticks ` surrounding the string and ${} surrounding the variables.
```javascript
let name = Jamie
`Hello ${name}!`
```