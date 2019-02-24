# Custom data types

Clio is a functional programming language, there isn't any plans for object oriented paradigm support, but you can define your custom types and objects and even have an init function for them.

Here's how to define a custom type:

```text
type Cat name age:
  name => self.name
  age => self.age

#moki 6 -> Cat => moki
moki.name -> print
```

`self` refers to the current instance.

