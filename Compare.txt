
Sarah Twomey,
David Emily, and
Alyssa Nielsen


# Comparing Python and C# as Object Oriented Languages

## Language purpose/genesis 
### Python
Python was implemented in late 1989. The language was invented to be a language capable of exception handling and to interact with the Amoeba operation system. In 2000, the Python 2.0 was introduced to include a cycle-detecting garbage collector, support for Unicode, and for a shift to a community-based development process.

The language was created to replace the language ABC. It has become popular on its own though due its easability in reading, object-orientation, structured programming, functional programming, and ability to be used as a scripting language.

### C#
Microsoft created C# as a replacement for Java with syntax similar to C and C++.  Hejlsberg is C#'s principal designer and lead architect at Microsoft, and was previously involved with the design of Turbo Pascal, Embarcadero Delphi, and Visual J++. In interviews and technical papers he has stated that flaws in most major programming languages (e.g. C++, Java, Delphi, and Smalltalk) drove the fundamentals of the Common Language Runtime (CLR), which, in turn, drove the design of the C# language itself.

Since the release of C# 2.0 in November 2005, the C# and Java languages have evolved on increasingly divergent trajectories, becoming two very different languages. One of the first major departures came with the addition of generics to both languages, with vastly different implementations.

Furthermore, C# has added several major features to accommodate functional-style programming, culminating in the LINQ extensions released with C# 3.0 and its supporting framework of lambda expressions, extension methods, and anonymous types. These features enable C# programmers to use functional programming techniques, such as closures, when it is advantageous to their application.

## Unique Features

### Python
While the Python language has evolved over the years by taking in aspects of other languages, it does have a few specific features. First, Python explicitly passes self as a form of a parameter to object member functions. The language also combines things such as data entry - prompting the user for entry and reading it in - to a simple function called 'input()'. Finally, the language incorporates a large number of datatypes such as ordereddict, namedtupke, array, list, tuple, diction, etc; making it popular in the scientific community. 

### C# 
Some unique features of C# include:
- Assemblies: This is a level of encapsulation above the typical namespaces or modules in most languages. Assemblies are similar to the idea of static/dynamic libraries in C or JAR files in Java. Notably, you can mark members as internal, which makes them public within the same assembly, but private to everybody outside the assembly. 
- Cross-language compatibility is first-class (not just for C): C# runs in the Common Language Runtime, which was designed from the beginning to support interoperability between languages.
- Properties are first-class: No longer need to write explicit getter and (optional) setter methods.
- Listeners are first-class: Classes can declare an event Foo with addFooListener and removeFooListener functionality built in.
- Foreign Methods are first-class: C# calls these extension methods.
- Partial Classes: Allows a class’s members to be defined in multiple files. Useful to add functionality to a generated class (for example, from a parser generator) without those modifications getting lost when the class is next regenerated.

## Name Spaces

### Python
Name spaces are implemented in Python by using a Dictionary -- Key to value lookup. Some examples of a Python name space are global names of a module, local names a function, built-in names such as abs() and cmp(). The name spaces exist only in the scope they are created.

### C#
.NET Framework uses namespaces to organize its many classes. The ```namespace``` keyword is used to declare a scope. The ability to create scopes within your project helps organize code and lets you create globally-unique types.  Declaring your own namespaces can help you control the scope of class and method names.
```
namespace  SampleNamespace  
{  
	class  SampleClass  
	{  
		public  void  SampleMethod()  
		{  
			System.Console.WriteLine(  
			"SampleMethod inside SampleNamespace");  
		}  
	}  
}
```
## Types

### Python
Python accomodates numeric types such as int, long and float. It also includes some built-in data types such as dictionary, list, set, and tuple. The determination of value or reference in Python is difficult as everything is an object in this language. This means that while the language is passed by value, the value is a reference, or pointer, to the specific object. An easier way to look at values and references in Python is to think of them just names, with the mutable or immmutatable being important. If the passed names are mutatable, they can be rebranded to be anything they need. 

Types in Python can be created or altered. In fact, everything object in Python can be extended to include addictional functions or change the default functions. 

### C#
C# is a strongly-typed language. Every variable and constant has a type, as does every expression that evaluates to a value. Every method signature specifies a type for each input parameter and for the return value. The .NET class library defines a set of built-in numeric types as well as more complex types that represent a wide variety of logical constructs, such as the file system, network connections, collections and arrays of objects, and dates. A typical C# program uses types from the class library as well as user-defined types that model the concepts that are specific to the program's problem domain.  C# also supports generics.

Instances of value types do not have referential identity nor referential comparison semantics - equality and inequality comparisons for value types compare the actual data values within the instances, unless the corresponding operators are overloaded. Value types are derived from System.ValueType, always have a default value, and can always be created and copied. Some other limitations on value types are that they cannot derive from each other (but can implement interfaces) and cannot have an explicit default (parameterless) constructor. Examples of value types are all primitive types, such as int (a signed 32-bit integer), float (a 32-bit IEEE floating-point number), char (a 16-bit Unicode code unit), and System.DateTime (identifies a specific point in time with nanosecond precision). Other examples are enum (enumerations) and struct (user defined structures).

In contrast, reference types have the notion of referential identity - each instance of a reference type is inherently distinct from every other instance, even if the data within both instances is the same. This is reflected in default equality and inequality comparisons for reference types, which test for referential rather than structural equality, unless the corresponding operators are overloaded (such as the case for System.String). In general, it is not always possible to create an instance of a reference type, nor to copy an existing instance, or perform a value comparison on two existing instances, though specific reference types can provide such services by exposing a public constructor or implementing a corresponding interface (such as ICloneable or IComparable). Examples of reference types are object (the ultimate base class for all other C# classes), System.String (a string of Unicode characters), and System.Array (a base class for all C# arrays).

Both type categories are extensible with user-defined types.

## Classes

### Python 
Classes in Python are created by using the 'class' keyword, the class name, and then a colon before inserting everything needed in the class.
For example:
```
class Car:
  def drive(self):
    print("This car is being driven.")
```
Creates a car class with the drive function.

To instantiate a new instance of the class, the user would create a variable and assign it to the class;:
```
x = Car()
```
This calls the '__init__()' function on the class. This function can be extended if the creator wanted the instance to do additional features, such as assign variable or run additional functions, in the instantiation period.
To de-initialize a class in Python the developer can use the close function on an object. This will delete the reference to the object. If the developer wanted to reuse the object in a pool, the developer could modify the close function to just erase the data inside. 

### C# 
Use class keyword to define a class.
```
public  class  Customer  
{  
// Fields, properties, methods and events go here...  
}
```
The new keyword is used to create a new instance.
```
Customer object1 = new Customer();
```
Constructing/initializing:
```
   // Constructor that takes no arguments.
    public Person()
    {
        name = "unknown";
    }

    // Constructor that takes one argument.
    public Person(string nm)
    {
        name = nm;
    }
```
C# also implements destructing/de-initializing.  Finalizers are used to destruct instances of classes.  Finalizers cannot be defined in structs, are only used with classes, a class can only have one finalizer, finalizers cannot be inherited or overloaded, finalizers cannot be called (they are invoked automatically), and a finalizer does not take modifiers or have parameters.

For example, the following is a declaration of a finalizer for the Car class.
```
class Car
{
    ~Car()  // destructor
    {
        // cleanup statements...
    }
}
```

## Instance reference name in data type (class) 

### Python
Python uses the 'self' keyword to reference the name of the data type. Python is special in that self doesn't need to be added to the signature as each object recognizes the current instance as 'self'

### C#
C# uses the 'this' keyword for the instance reference name in the class. 
```
public Employee(string name, string alias)
{
    // Use this to qualify the fields, name and alias:
    this.name = name;
    this.alias = alias;
}
```
## Properties

### Python
Using 'getters' and 'setters' aren't typically used in Python but can be utilized. The typical way is just to use plain attributes to pass the information and then to dereference the attribute using the 'del' function.
However, getters and setters can be added to the code to make it consistent to other programming. These can be added using the 'property' decorator without altering the original code
```
class obj:
  @property
  def attribute(self):
    return self.__attribute
  @attribute.setter
  def attribute_setter(self, value):
    self.__attribute = value
 ```
 ### C#
##### Getters and setters

Properties enable a class to expose a public way of getting and setting values, while hiding implementation or verification code.  A get property accessor is used to return the property value, and a set accessor is used to assign a new value. These accessors can have different access levels.

The value keyword is used to define the value being assigned by the set accessor:
```
private string _s;

public string YourProperty
{
get { return _s; }
set { _s = value; }
}
```
Properties that do not implement a set accessor are read only:
```
public string YourProperty
{
get { return "somestring..."; }
}
```
For simple properties that require no custom accessor code, you can use auto-implemented properties.  Getters and Setters are built in to auto-implemented properties in C.
```
public class ClassName
{
    public string YourProperty { get; set; }
}
 ```
##### Backing variables
C# has backing variables built in/ hidden, but they can be managed manually if needed.

Pre .NET 3.5:
```
private string _something; 
public string Something 
{ 
	get { 
		return _something; 
		} 
	set { 
		_something = value; 
		} 
}
```
Or more recent: ```public string Something { get; set; }```

##### Computed properties
C# allows computed properties. An example:
```
class TimePeriod
{
   private double seconds;

   public double Hours
   {
       get { return seconds / 3600; }
       set { 
          if (value < 0 || value > 24)
             throw new ArgumentOutOfRangeException(
                   $"{nameof(value)} must be between 0 and 24.");

          seconds = value * 3600; 
       }
   }
}
```
 ## Interfaces / protocols
 
 ### Python
 Python doesn't use interfaces or protocols, as it uses the idea of duck-typing. Duck-typing is applying the idea of "if it looks like a duck, it must be a duck", in programming. This comparison is done at runtime and is handled by the type checking. Generally if the object type and methods work, the interface will work; else a exception will be thrown.
 
 ### C#
C# supports interfaces.  By using interfaces, you can include behavior from multiple sources in a class.  It is used as a workaround because C# doesn't support multiple inheritance of classes. It uses the ```interface``` keyword.
```
interface IEquatable<T>
{
    bool Equals(T obj);
}
```
## Inheritance / extension

### Python
Inheritance in Python is handled by inluding the parent in the parenthesis after a class declaration.
```
class Person(object):
  def foo(self):
  ...
class Waiter(Person):
  ...
```
In this example, Person is inheriting from Object and Waiter is inheriting from Person. A waiter can use the Person's foo method by using "super().foo()" or by calling it as "Person.greet(self)" from Waiter.

### C#
C# and .NET support single inheritance only. However, inheritance is transitive, which allows you to define an inheritance hierarchy for a set of types.  
```
public class A 
{
   private int value = 10;

   public class B : A
   {
       public int GetValue()
       {
           return this.value;
       }     
   }
}
```

Extension methods enable you to "add" methods to existing types without creating a new derived type, recompiling, or otherwise modifying the original type. Extension methods are a special kind of static method, but they are called as if they were instance methods on the extended type. For client code written in C#, F# and Visual Basic, there is no apparent difference between calling an extension method and the methods that are actually defined in a type.

## Reflection

### Python
Reflection refers to the ability of the language to tell attributes about objects that might be passed as parameters to a function. Python is dynamically typed so this ability is important. Using "type(obj)" will return the type of the object in question. Python also has other commands available to assist in reflection. Python uses the "Isinstance()" command to test if an object is an instance of a type or class. The "getattr()" command can return a value of an attribute of an object.

### C#
With C#, you can use reflection to dynamically create an instance of a type, bind the type to an existing object, or get the type from an existing object and invoke its methods or access its fields and properties. If you are using attributes in your code, reflection enables you to access them.

Reflection is useful in the following situations:
- When you have to access attributes in your program's metadata.
- For examining and instantiating types in an assembly.
- For building new types at runtime. Use classes in System.Reflection.Emit.
- For performing late binding, accessing methods on types created at run time.

## Memory Management

### Python
Python stores all objects and data structures in a private heap. This heap is controlled by the Python memory manager, which deals with sharing, segmentation, preallocation, and cachine.
In addition, Python uses reference counting and garbage collection to maintain memory usage. 
##### Reference Counting 
Reference counting is the idea that an object needs to be maintained when the count of that object is greater than 0. 
##### Garbage Collection
Garbage collection is automatic in Python and happens when the code can no longer 'reach' an object. Examples of garbage collection are when "del" is used on an object or when an object is set equal to None(Null). Garbage collection is typically performed automatically but can be manually called by using "gc.collect()"

### C# 
For the majority of the objects that your app creates, you can rely on .NET's garbage collector to handle memory management. 

The Microsoft .NET common language runtime requires that all resources be allocated from the managed heap. Objects are automatically freed when they are no longer needed by the application.

When a process is initialized, the runtime reserves a contiguous region of address space that initially has no storage allocated for it. This address space region is the managed heap. The heap also maintains a pointer. This pointer indicates where the next object is to be allocated within the heap. Initially, the pointer is set to the base address of the reserved address space region.

An application creates an object using the new operator. This operator first ensures that the bytes required by the new object fit in the reserved region (committing storage if necessary). If the object fits, then the pointer points to the object in the heap, this object's constructor is called, and the new operator returns the address of the object.

##### Reference Counting
Reference counting is the idea that an object needs to be maintained when the count of that object is greater than 0.

##### Garbage Collection
The garbage collector checks to see if there are any objects in the heap that are no longer being used by the application. If such objects exist, then the memory used by these objects can be reclaimed. (If no more memory is available for the heap, then the new operator throws an OutOfMemoryException.)

In the common language runtime, the managed heap always knows the actual type of an object, and the metadata information is used to determine which members of an object refer to other objects.

##### Automatic reference counting?
Not used in C# (it uses Garbage Collection) - an e-mail from Brian Harry explains why:

> “We initially started with the assumption that the solution would take the form of automatic ref counting (so the programmer couldn't forget) plus some other stuff to detect and handle cycles automatically. ...we ultimately concluded that this was not going to work in the general case.
...
 In summary:
We feel that it is very important to solve the cycle problem without forcing programmers to understand, track down and design around these complex data structure problems.
We want to make sure we have a high performance (both speed and working set) system and our analysis shows that using reference counting for every single object in the system will not allow us to achieve this goal.
For a variety of reasons, including composition and casting issues, there is no simple transparent solution to having just those objects that need it be ref counted.
We chose not to select a solution that provides deterministic finalization for a single language/context because it inhibits interop with other languages and causes bifurcation of class libraries by creating language specific versions.

## Comparisons of References and Values
### Python
Python uses "==" and "is" for comparing references and values.  

In Python, "==" refers to value equality. This is for checking if two objects have the same value. On the other hand, "is" refers to reference equality. This is used when checking if two references refer to the same object.
```
a = 500
b = 500
a == b # returns True
a is b # returns False
```
### C# 
"Equals" and "==" will compare by reference by default if they're not overriden / overloaded in a subclass. ReferenceEquals will always compare by reference.  ```String.Compare``` a compares two specified String objects and returns an integer that indicates their relative position in the sort order.  ```String.CompareTo``` compares this instance with a specified object or String and returns an integer that indicates whether this instance precedes, follows, or appears in the same position in the sort order as the specified object or String.

Strings overload == to implement value equality; also, since they're immutable, C# will generally reuse the same instance for the same literal string. 
```
C# program that compares strings for equality

using System;

class Program
{
    static void Main()
    {
        string a = "a" + 1;
        string b = "a" + 1;

        // 1
        // Compare a to b using instance method on a.
        if (a.Equals(b))
        {
            Console.WriteLine("a.Equals(b) = true");
        }

        // 2
        // Compare b to a using instance method on b.
        if (b.Equals(a))
        {
            Console.WriteLine("b.Equals(a) = true");
        }

        // 3
        // Compare a to b with op_Equality
        if (a == b)
        {
            Console.WriteLine("a == b = true");
        }

        // 4
        // Compare with string.Compare; this returns zero if they are equal
        if (string.Compare(a, b) == 0)
        {
            Console.WriteLine("string.Compare(a, b) = 0");
        }

        // 5
        // Compare with string.CompareOrdinal
        // This returns zero if the char numeric values are equal
        if (string.CompareOrdinal(a, b) == 0)
        {
            Console.WriteLine("string.CompareOrdinal(a, b) = 0");
        }

        // 6
        // Compare with instance Compare method
        if (a.CompareTo(b) == 0)
        {
            Console.WriteLine("a.CompareTo(b) = 0");
        }
    }
}

Output

a.Equals(b) = true
b.Equals(a) = true
a == b = true
string.Compare(a, b) = 0
string.CompareOrdinal(a, b) = 0
a.CompareTo(b) = 0
```
## Null/Nil references
### Python
Python uses the "None" singleton instead of Null or Nil. Objects can be assigned to None.
### C# 
C# utilizes ```null``` (versus Nil or none).  The ```null``` keyword is a literal that represents a null reference, one that does not refer to any object. Null is the default value of reference-type variables. Ordinary value types cannot be null. However, C# 2.0 introduced nullable value types.
```
        string s = null;
```


## Errors and exception handling
### Python 

### C#
A try block is used by C# programmers to partition code that might be affected by an exception. Associated catch blocks are used to handle any resulting exceptions. A finally block contains code that is run regardless of whether or not an exception is thrown in the try block, such as releasing resources that are allocated in the try block. A try block requires one or more associated catch blocks, or a finally block, or both.
```
try
{
    // Code to try goes here.
}
catch (SomeSpecificException ex)
{
    // Code to handle the exception goes here - like 
“throw new System.ArgumentOutOfRangeException("Parameter index is out of range.", e);”
}
finally
{
    // Code to execute after the try (and possibly catch) blocks 
    // goes here.
} 
```


## Lambda
### Python
Lambda functions were added to Python because of increased demand from Lisp programmers. Lambdas are easily assigned in Python:
```
f = lambda x, y : x + y
f(1,1) # returns 2
```
This functional programming is especially useful with Python's list comprehension and is normally used with functions such as "map()", "filter()", and "reduce()"
In addition to lambdas, functions are treated as first-class objects and can be passed as an argument or return value to another function object.
### C#
C# implements Lambda expressions,  By using lambda expressions, you can write local functions that can be passed as arguments or returned as the value of function calls. Lambda expressions are particularly helpful for writing LINQ query expressions.
C# uses lambda expressions that look like: 

	(input-parameters) => expression
	
and uses delegates instead of functions as types. 
```
public delegate void DoSomethingDelegate(Object param1, Object param2);

delegate int del(int i);  
static void Main(string[] args)  
{  
    del myDelegate = x => x * x;  
    int j = myDelegate(5); //j = 25  
}  
```

## Listeners or Event Handlers
### Python
Python's open source nature has led to a large number of different frameworks that handle events. The most popular include: pydispatcher, zope.event, EventHook, Event class, Pynotify, and louie. The different ways come with different benefits and difficulties.
For example, the EventHook can be simply added to an existing class upon initialization:
```
class MyBroadcaster()
  def __init__():
    self.onChange = EventHook()

theBroadcaster = MyBroadcaster()
# add a listener to an event
theBroadcaster.onChange += myFunction()
```
Please look at the associated documentation to choose which one may work best for different environments.
### C#
Events in the .NET Framework are based on the delegate model. The delegate model follows the observer design pattern, which enables a subscriber to register with, and receive notifications from, a provider. An event sender pushes a notification that an event has happened, and an event receiver receives that notification and defines a response to it.

To respond to an event, you define an event handler method in the event receiver. This method must match the signature of the delegate for the event you are handling. In the event handler, you perform the actions that are required when the event is raised, such as collecting user input after the user clicks a button. To receive notifications when the event occurs, your event handler method must subscribe to the event.
```
class Program
{
    static void Main(string[] args)
    {
        Counter c = new Counter();
        c.ThresholdReached += c_ThresholdReached;
        // provide remaining implementation for the class
    }

    static void c_ThresholdReached(object sender, EventArgs e)
    {
        Console.WriteLine("The threshold was reached.");
    }
}
```
## Singleton
### Python
Singletons are less common in Python when compared to a language like Java. Python, by nature, does not have the "final" keyword that Java uses to enforce a singleton. Singleton can be made in Python though by using different methods, including creating a dictionary of "instances" and enforcing only one can be made.
For example:
```
def singleton(cls):
  instances = {}
  def getInstance():
    if cls not in instances:
      instances[cls] = cls()
    return instances[cls]
  return getInstance
```
Using a pattern like that above enforces a psuedo final keyword as the function will return the current singleton if more than one singletons are attempted to be created.
### C# 
Implementation of Singleton in C# looks like the following:
- Common, non-treadsafe way:

```
public sealed class Singleton
{
    private static Singleton instance=null;
    private Singleton(){}
    public static Singleton Instance {
        get
        {
            if (instance==null)
            {
                instance = new Singleton();
            }
            return instance;
        }
    }
}
```
- To make it thread safe: 
```
public sealed class Singleton
{
    private static Singleton instance = null;
    private static readonly object padlock = new object();
    Singleton(){}
    public static Singleton Instance
    {
        get
        {
            lock (padlock)
            {
                if (instance == null)
                {
                    instance = new Singleton();
                }
                return instance;
            }
        }
    }
}
```
- The singleton instance can be lazily instantiated:
```
public sealed class Singleton
{
    private static readonly Lazy<Singleton> lazy =
        new Lazy<Singleton>(() => new Singleton());
    
    public static Singleton Instance { get { return lazy.Value; } }

    private Singleton() { }
}
```
- another way to lazy instantiate: 
```
public sealed class Singleton
{
    private Singleton(){ }

    public static Singleton Instance { get { return Nested.instance; } }
        
    private class Nested
    {
        // Explicit static constructor to tell C# compiler
        // not to mark type as beforefieldinit
        static Nested(){ }
        internal static readonly Singleton instance = new Singleton();
    }
}

```

## Procedural Programming
### Python
Python does support procedural programming. Python is one of the few object oriented languages that does not enforce the idea that code be written in a OO style. Utilizing procedural programming allows Python to be written using a 'step-by-step' style, similiar to programming in C or C++.
### C# 
C# was designed to primarily support imperative (procedural) programming.

## Functional Programming
### Python
Python supports functional programming. The FP ability was later added to Python, which means it can be programmed in the same style as more popular functional languages such as Haskell and OCaml. Programming in a functional style allows Python to not save 'side effects', or functions that modify internal state. Programming in 'pure' functional programming normally is not done in Python though, but instead functional programming functions will be added in in support of other features.
### C# 
C# includes explicit language extensions to support functional programming, including lambda expressions and type inference. LINQ technology is a form of declarative, functional programming.

## Multithreading
### Python
Python supports multithreading through different modules and libraries, most notably the "threading" module.
```
import threading
t1 = threading.Thread(target, args)
t1.start()
t1.join()
```
Using multithreading allows large tasks to be split up into smaller tasks to be accomplished separately and takes advantage of a CPU's ability to handle multiple processes.

### C# 
C# implements multithreading using the .NET Framework ```System.Threading``` namespace to create and control threads, sets its priority, and gets its status. C# programs have one thread by default. However, other threads can then be created and used to execute code in parallel with the primary thread.
