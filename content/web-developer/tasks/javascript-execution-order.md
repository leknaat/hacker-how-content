##Example

Write the execution order of:

```
Math.sum([1,2,3, [1,2,3].length])
```
Answer:
```
1
// => 1
2
// => 2
3
// => 3

1
// => 1
2
// => 2
3
// => 3
[1,2,3]
// => [1,2,3]
[1,2,3].length
// => 3

Math.sum([1, 2, 3, 4])
// => 10
```

##1

[1, 2, 3, 4]

##2
```
"hello".subString(0, 3).length
```


##3

```
"hello".subString(0, 3 - 1).length + "world"
```

##4

```
{ hello: "wor" + "ld" }
```
