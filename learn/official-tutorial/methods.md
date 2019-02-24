# Methods

Sometimes you want to overload a function for a custom data type and access inner properties of the instance. Clio provides a syntax for this:

```text
type Cat name age:
  name => self.name
  age => self.age

type Dog name age:
  name => self.name
  age => self.age

@eager
fn hello person of Cat:
  #Meow! #Hello person -> print
  'My name is' self.name -> print

fn hello person of Dog:
  #Woof! #Hello person -> print
  'My name is' self.name -> print

#Moki 6 -> Cat -> hello #Pouya
#Gino 6 -> Dog -> hello #Pouya
```

