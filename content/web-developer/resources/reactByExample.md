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

## React

React lets you write functions which return JSX. It then puts that JSX/HTML inside your web browser (on the screen). 

### Stateless Functional Components (Not covered in code school).

```
const Banana = () => <p>Banana</p> 
```

We call `Banana` a **component**. Components start with capital letters.

You can use this inside another component like this:

```
const FruitBowl = () => <Banana /> // Renders <p>Hello</p> on the screen
```

`<Banana />` is a special syntax for calling the function we defined above. 

`<Banana /> === Banana()`
