# MasMas.js  
The functions you need in JS that aren't provided!  

## Setup  

Download MasMas.js from our [GitHub repository][GitHub Main].  Then, unzip the file, and add it to your project.
In the HTML head, put:
```html
<script src="masmas.js" type="text/javascript"></script>
```

## Documentation  

### isFloat & isInteger
Checks to see if number passed is float or int. Takes the true value of the number:
```js
isInt(5) //returns true
isInt(5.0) //returns true
isFloat(5) //returns false
isFloat(5.0) //returns false
isFloat(5.2) //returns true
```

### Int and Float types!
You can now use 64-bit int and 64-bit float types in your code:
```js
var anInt = Int(5) //anInt is 5
var anInt = Float(5) //Throws error
var anInt = Float(5.2) //anInt is 5.2
```
### The A function
JS float addition has always been a bit finicky.
The A function solves all that:
```js
var num = 0.1+0.2 //Returns 0.30000000000000004 - ummm... what?
var num = (0.1+0.2).A() //Returns 0.3 - Much better!
```
### "Repeat" Loops
A syntatic sugar trademark has been to make loops that look GOOD. MasMas comes with two such loops:
```js
(3).times(()=>{
  console.log("Hello World!")
});
execute(3, ()=>{
  console.log("Hello World!")
});
//These do the same thing! 
```
However, using execute is recommended because support for *times* is shaky.
### Rounding... why didn't JS have this from the start?
This is pretty much self-explanatory.
```js
  (3.2).round() //returns 3
  (3.24).round(1) //returns  3.2 - you can specifiy digits to round to.
```
### String splicing - inserting code in the middle of a string!
Insert characters in the middle of a string!
```js
("Hello World").splice(0/*index*/, 0/*just put zero for this one*/, "Hi") //returns "HiHello World"
```
[GitHub Main]: https://github.com/MasMas-js/MasMas.js
