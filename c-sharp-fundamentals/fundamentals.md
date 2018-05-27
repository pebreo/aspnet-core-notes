
# Syntax

access modifiers:
public, private, internal, protected
protected - cannot override a method inside an abstract class

inheritance:
abstract and interface

polymorphism

OOP

'this' keyword

```
async myfunc() {
    await foo();
}
```

# Linq

myList.where().select()

myList.Except(myList2)

myList.Union(myList2)



# Delegates
delegate - function contract

```
js
var myfunc = function() {
  return 1;
}

c#
public delegeate int PaulDelegate();

PaulDelegate myfunc = PaulDelegateMethod;

// implement
int PaulDelegateMethod()
{
    return 1;
}
// using lambdas, same thing
PaulDelegate myfunc = () => {
    return 1;
}
```

#### or, without the signature (declaration of the delegate)
```
myfunc = () => {
  return 1;
}

or if you need the type for the param and/or the return type

int myfunc = (int foo) =>
{
 return 1;
}
```

when doing event handler, you will use delegates to customize your event handlers.


# Misc.

backlog refinement

retrospectives

threading/tasks (async,await)

google: vscode intellisense

google : csharp event handler

https://www.youtube.com/results?search_query=time+management+for+developers

#

# Resources

augury - angular

https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers

https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/members


