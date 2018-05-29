
### Syntax

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

### Linq

myList.where().select()

myList.Except(myList2)

myList.Union(myList2)



### Delegates
Think of delegates as function contracts.

Similar to VoidCallback in Dart.

Why are delegates useful?
Because when working with event handlers, you will use delegates to 
customize your event handlers.

```
//js
var myfunc = function() {
  return 1;
}

// C#
public delegate int PaulDelegate(); // a contract 

PaulDelegate myfunc = PaulDelegateMethod;

// implement the contract with a normal function declaration
int PaulDelegateMethod()
{
    return 1;
}
// Or you can use lambdas to implement the delegate
PaulDelegate myfunc = () => {
    return 1;
}
```

Note: You don't have to use delegates because 
you can have  
```
// default input is void and return type is declared as integer
// so, the following still shows the developer the same relevant information 
// that the delegate declaration shows
int myfunc = () => {
  return 1;
}
```



### Misc.

backlog refinement

retrospectives

threading/tasks (async,await)

google: vscode intellisense

google : csharp event handler

https://www.youtube.com/results?search_query=time+management+for+developers


### Resources

augury chrome extension - angular

https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers

https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/members


