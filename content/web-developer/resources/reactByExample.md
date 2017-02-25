# React

### JSX

Think of JSX as a new type in Javascript (It will only work whilst using webpack).

```
const banana = "banana"
const appleCount = 1 
const myArray = []
const myObject = {hello: 1}
const someHtml = <p>Hello!</p> // <- JSX
```

Notice there are no quotes around it. It's not a string. It's a whole new type.


### Differences from normal HTML

#### Attribute names are different

* They're [camel cased](https://en.wikipedia.org/wiki/Camel_case)
* Sometimes they're a tiny bit different from normal HTML [Read more](https://facebook.github.io/react/docs/tags-and-attributes.html)

A good example is `class="my-css-class"`

e.g.

```
HTML                                               JSX
<button class="my-css-class">Click Me</button> -> <button className="my-css-class">Click Me</button>
```

#### You can write Javascript inside your JSX.

JSX works just like normal HTML unless you do one thing. If you put `{}` then inside the brackets you go back to javascript.

```
var x = 1
var someHtml = <div>{x + 1}</div>
// => <div>2</div>
```

```
var buttonClass = 'my-css-class'
var button  = <button className={buttonClass}>Click Me</button>
//=> <button className="my-css-class">Click Me</button>
```

*Exception*
It's quite rare to use it though.
```
var elementType = 'div'
var someHtml = <elementType></elementType>
// => <div></div>
```
#### JSX in JSX

Since JSX is just javascript (it's a new type remember!)

You can also put that inside `{}`

```
const apple = <p>Apple!</p>
<div>{apple}</div>
// => <div><p>Apple!</p></div>
```

#### Arrays in JSX

If you use `{}` with an array. JSX will put each thing in the array one after the other.

```
const fruits = [
  <p>Apple</p>,
  <p>Banana</p>,
  <p>Pear</p>
]
<div>{fruits}</div>
// => <div><p>Apple</p> <p>Banana</p> <p>Pear</p></div>
```

This makes `map` **really** useful:

```
const numbers = [1, 2, 3]
const numbersJSX = _.map(numbers, (number) => <p>{number}</p>) // Returns [<p>1</p>, <p>2</p>, <p>3</p>] 
<div>{numbersJSX}</div>
// =>  <div><p>1</p> <p>2</p> <p>3</p></div>
```


## React

React takes functions which return JSX, evalutes them, and puts that JSX/HTML inside your web browser (on the screen). 

### Stateless Functional Components (Not covered in code school).

```
const Banana = () => <p>Banana</p> // Just a lambda that returns some JSX
```

We call `Banana` a **component**. Components start with capital letters.

You can use this inside another component like this:

```
const FruitBowl = () => <Banana /> // Renders <p>Hello</p> on the screen
```

`<Banana />` is a special syntax for calling the function we defined above. 

`<Banana />` is like saying: `Banana()`

#### With Props

Props is an object which contains all the arguments to our component.

```
const Cat = (props) => <p>Meow my name is: {props.name}</p> 
```
`props` comes in as a parameter in your lambda. 

```
const Geoff = () => <Cat name={'Geoff'} /> // Renders <p>Meow my name is: Geoff</p> on the screen
```

In this case we're calling our `Cat` function with a single prop: `name` with a value of `'Geoff'`.

`<Cat name={'Geoff'} />` is like saying: `Cat({name: 'Geoff'})`
Both would return `<p>Meow my name is: Geoff</p>`


