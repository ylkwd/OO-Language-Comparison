# Classes
* A class can contain any of the following variable types in **Java**

	* Local variables − Variables defined inside methods, constructors or blocks are called local variables. The variable will be declared and initialized within the method and the variable will be destroyed when the method has completed.

	* Instance variables − Instance variables are variables within a class but outside any method. These variables are initialized when the class is instantiated. Instance variables can be accessed from inside any method, constructor or blocks of that particular class.

	* Class variables − Class variables are variables declared within a class, outside any method, with the static keyword.
```java
public class Dog {
   String breed;
   int ageC
   String color;

   void barking() {
   }

   void hungry() {
   }

   void sleeping() {
   }
}
```
* **Swift** are building blocks of flexible constructs. Similar to constants, variables and functions the user can define class properties and methods. **Swift** provides us the functionality that while declaring classes the users need not create interfaces or implementation files. **Swift** allows developers to create classes as a single file and the external interfaces will be created by default once the classes are initialized.
```swift
class student {
   var studname: String
   var mark: Int 
   var mark2: Int 
}
let studrecord = student()
class MarksStruct {
   var mark: Int
   init(mark: Int) {
      self.mark = mark
   }
}

class studentMarks {
   var mark = 300
}
let marks = studentMarks()
println("Mark is \(marks.mark)")
```

