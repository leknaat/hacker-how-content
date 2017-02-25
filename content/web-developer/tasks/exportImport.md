#Exporting and Importing
Setup

Checkout https://github.com/z-dev/react-seed and follow the instructions in the `readme.md`

Once it's up and running go to http://localhost/importExportTasks.

`import` and test your answers in `src/components/importExport/index.js`

All your answers should go in the `src/components/importExport` 

1. 

`export default` a string: "Banana!" in a file `banana.js`

import it and `console.log` it in `src/components/importExport/index.js`


2.

In addition to a) `export` a `const` called `apple` which contains a string: "Apple!" in a file `apple.js`

import it and `console.log` it in `src/components/importExport/index.js`


3.

`export default` a function in a file `myFunctions.js`

The function should take two numbers and return the result of adding them together.

import it and `console.log` the output in `src/components/importExport/index.js`.

4.

Create a file `fruits.js`

Add an export default of a string `'Get your fruits here'`

Add two exported consts `apple` and `banana`

Import all three and `console.log` the output in `src/components/importExport/index.js`.

5.

Create a folder `pies`

Then in `src/components/importExport/index.js`, make this work:
```
import pieMenu, {applePie, blueberryPie} from './pies'

console.log(pieMenu)
// prints "Apple Pie, Blueberry Pie"
console.log(applePie)
// prints "Apple Pie"
console.log(blueberryPie)
// prints "Blueberry Pie"
```
