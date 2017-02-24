#Exporting and Importing

You've learned to write Javascript. Congrats!

So far you put code into `.js` files then used `<script src="myfile.js" />` to load them in the HTML.

Webpack is a magical beast. It takes all your `.js` files and 'inlines' (merges) them into one big file (how clever).

It then automatically adds one `<script src"oneMassiveJavascriptFile.js" />` to your HTML for you. 

## Why export and import?

You can write all your code in one giant file. It will work, but it just gets confusing once you have a 3000 line file. In general we like to have files which are less than 2 screen heights.

This is only to help human beings understand what the hell is going on. Javascript doesn't care if you break it up, because it's a computer.

## Export Default

### How it works

* You can only `export default` once per file. 
* It exports a expression not a declaration.


`export default "Banana"`

`export default 1`

`export default [1,2,3]`

`export default {hello: "world"}`

`export default (a, b) => a + b` <--- functions are good :)

`export default (a, b) => { return a + b }`

`export default const x = 1` <----ERROR can't export a const.

You can then import your `export default`'d expression in another file.

e.g. 

```
import hello from './hello'

console.log(hello) // <--- hello is just var in your program now :)
```

Importing an exported default, you can name the import var whatever you like.

```
import hello123 from './hello'

console.log(hello123) // <--- hello123 is not named like the original.
```

### Examples

1.

`myFolder/banana.js`
```
export default "Banana!"
```


`myFolder/fruitBowl.js`
```
import banana from './banana'

console.log(banana) // => prints "Banana!"
```

2.

`myFolder/banana.js`
```
export default () => "Banana!" // Banana function
```


`myFolder/fruitBowl.js`
```
import banana from './banana'

//banana is a function (lambda)

console.log(banana()) // => prints "Banana!"
```

3.

`myFolder/maths.js`
```
export default (a, b) => a + b // Banana function
```


`myFolder/doSomeMaths.js`
```
import adder from './maths'

//adder is a function (lambda)

console.log(adder(1, 2)) // => prints 3
```


### Exporting a const
`export const apples = 
