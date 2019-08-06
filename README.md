### The functions you need in JavaScript that aren't provided!  

An ever-growing supply of the best functions and classes, found and made by people from different places in the world!

> **MasMas.js IS NO LONGER BEING ACTIVELY DEVELOPED**. The library is still open for use though.

--------------

## Setup  

Download MasMas.js from our [GitHub repository][GitHub Main].  Then, unzip the file, and add it to your project.
In the HTML head, put:
```html
<script src="masmas.js" type="text/javascript"></script>

<script>
  // Or you can use GitHub's servers to load the script in, no download required!
</script>

<script src="https://raw.githubusercontent.com/MasMas-js/MasMas.js/master/masmas.js" type="text/javascript"></script>
```

## Documentation  

### Check if MasMas is loaded 

To see if MasMas.js is loaded on your page, you can run:

```js
// isLoaded will return true if it is loaded
if(isLoaded) console.log('MasMas.js says hello world!');
else console.log('MasMas.js isn\'t loaded, how sad.');
```

### `isFloat` & `isInteger`  

Checks to see if number passed is a float/int depending on which function you use.  Takes the true value of the number as a parameter:
```js
isInt(5);     // returns true
isInt(5.0);   // returns true
isFloat(5);   // returns false
isFloat(5.0); // returns false
isFloat(5.2); // returns true
```

### `Int` and `Float` types!  

You can now use 64-bit int and 64-bit float types in your code:
```js
var anInt = Int(5);     // anInt is 5
var anInt = Float(5);   // Throws error
var anInt = Float(5.2); // anInt is 5.2
```

### The `A` function  

JavaScript float addition has always been a bit finicky.
The `A` function solves all that:
```js
var num = 0.1+0.2;       // Returns 0.30000000000000004 - ummm... what?!
var num = (0.1+0.2).A(); // Returns 0.3 - Much better!
```

### "`Repeat`" Loops  

A syntatic sugar trademark has been to make loops that look GOOD.  MasMas comes with two such loops:
```js
(3).times(() => {
  console.log("Hello World!");
});
execute(3, () => {
  console.log("Hello World!");
});
// These do the same thing! 
```
However, using `execute` is recommended because support for `times` is not the best.  

### Rounding  

Why hasn't JavaScript have this from the start?!  

This is pretty much self-explanatory.
```js
  (3.2).round();   // returns 3
  (3.24).round(1); // returns  3.2 - you can specifiy digits to round to.
```

### Commafy  

Add commas to numbers!  *This isn't in **ANY** languages*.  

```js
(1000).commafy(); // Returns 1,000
```

### String splicing - inserting code in the middle of a string!  

Insert characters in the middle of a string!
```js
("Hello World").splice(0/*index*/, 0/*just put zero for this one*/, "Hi") // returns "HiHello World"
```

### `global` Variables  

Define global variables from inside functions! (Without any worries about overriding something)
```js
function foo() {
  global("something", 5);
}
foo();
console.log(something); // Logs 5
```

### Exists  

Check if something exists:  
```js
var x;
exists(x); // returns false
```

### LocalStorage made easy!  

You can now create a variable stored in localStorage like this:
```js
localStore("variable", 5); // Remebers variable in localStorage and can update
```

### The `wrap` Function  

Basically an IIFE made easy + readable:
```js
wrap(() => {
  // Do stuff...
})
```

### `loadjQuery` & `loadScript`  

Include JavaScript files on the fly!
```js
loadjQuery();    // Now you have access to jQuery
loadScript(url); // Load another script by the url
// These raw methods are NOT suggested. Read the section below this text for more info.
```

However, if you just load the script, you won't have access to it for a little while. 
This can lead to unexpected errors. You can solve this by inserting a callback function to 
execute once the script is loaded:

```js
loadjQuery(function() { // Once jQuery is loaded, do something with it.
  $("body").html("jQuery was loaded!");
});

// Or with any other script:
loadScript(url, function() {
  console.log("Some cool script is now loaded!");
});
```

### `Random` class!  

Random numbers, made easy:
```js
var r = new Random();

// pass false for int, true for float
r.getRandomNumber(1, 10, false); // returns a random int
r.getRandomNumber(1, 10, true); // returns a random float
r.getRandomBool();
```

### Easy `canvas` interface  

Get a head start with the HTML5 canvas with the setupCanvas function.

```js
setupCanvas();
// canvas is document.getElementById("canvas");
// ctx is canvas.getContext('2d');
```

And then use the `MasMasCanvas` class to simplify canvas drawing:

```js
var can = new MasMasCanvas(ctx);
// And you get four nice methods to use:
can.rect(x, y, width, height);
can.ellipse(x, y, width height);
can.text(text, x, y);
can.fill("Color");
```

## Organization-wide documents  

When contributing to any repository in this organization, please keep in mind the content of the following documents:  
- [X] [Code of conduct][code of conduct]
- [X] [Contributing guidelines][contrib]

[code of conduct]: https://github.com/MasMas-js/MasMas.js/blob/master/.github/CODE_OF_CONDUCT.md
[contrib]: https://github.com/MasMas-js/MasMas.js/blob/master/.github/CONTRIBUTING.md
[GitHub Main]: https://github.com/MasMas-js/MasMas.js
