# Overloading

Overloading is the process of creating different versions of a function depending on the type of arguments they receive. Let's create an overloaded function and see how it works:

```text
@eager
fn greet text if str:
  'greetings textual' text -> print

fn greet number if num:
  'greetings numeric' number -> print

['Lorem ipsum' 42] -> * greet
```

Note that decorators are shared between overloads.

