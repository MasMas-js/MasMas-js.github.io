# MasMas.js  
The functions you need in JS that aren't provided!  

## Setup  

Download MasMas.js from our [GitHub repository][GitHub Main].  Then, unzip the file, and add it to your project.
In the HTML head, put:
```html
<script src="masmas.js" type="text/javascript"></script>
```

## Documentation  

### `isFloat` & `isInteger`
Checks to see if number passed is float or int. Takes the true value of the number:
```js
isInt(5) //returns true
isInt(5.0) //returns true
isFloat(5) //returns false
isFloat(5.0) //returns false
isFloat(5.2) //returns true
```

### `Int` and `Float` types!
You can now use 64-bit int and 64-bit float types in your code:
```js
var anInt = Int(5)      // anInt is 5
var anInt = Float(5)    // Throws error
var anInt = Float(5.2)  // anInt is 5.2
```

[GitHub Main]: https://github.com/MasMas-js/MasMas.js
