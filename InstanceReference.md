#Instance reference name in data type (class)
this? self?
## Java:
this refers to the current object.
Each non-static method runs in the context of an object. So if you have a class like this:
```Java
public class MyThisTest {
  private int a;

  public MyThisTest() {
    this(42); // calls the other constructor
  }

  public MyThisTest(int a) {
    this.a = a; // assigns the value of the parameter a to the field of the same name
  }

  public void frobnicate() {
    int a = 1;

    System.out.println(a); // refers to the local variable a
    System.out.println(this.a); // refers to the field a
    System.out.println(this); // refers to this entire object
  }

  public String toString() {
    return "MyThisTest a=" + a; // refers to the field a
  }
}

```
## Swift:
Every instance of a type has an implicit property called self, which is exactly equivalent to the instance itself. You use the self property to refer to the current instance within its own instance methods.
The increment() method in the example above could have been written like this:

```Swift
func increment() {
self.count += 1	
}
```
