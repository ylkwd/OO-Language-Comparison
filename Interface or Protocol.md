# Interfaces / protocols
What does the language support?
What abilities does it have?
How is it used?

## Java:
Java support interface
An interface is a reference type in Java. It is similar to class. It is a collection of abstract methods. A class implements an interface, thereby inheriting the abstract methods of the interface.
Along with abstract methods, an interface may also contain constants, default methods, static methods, and nested types. Method bodies exist only for default methods and static methods.
### For declaring interface:
```Java
public interface Animal {
   public void eat();
   public void travel();
}
```
### For using interface:
```Java
public class MammalInt implements Animal {
   public static void main(String args[]) {
      MammalInt m = new MammalInt();
      m.eat();
      m.travel();
   }
}
```
## Swift:
Swift support protocol
A protocol defines a blueprint of methods, properties, and other requirements that suit a particular task or piece of functionality. The protocol can then be adopted by a class, structure, or enumeration to provide an actual implementation of those requirements. Any type that satisfies the requirements of a protocol is said to conform to that protocol.
```Swift
protocol classa {

   var marks: Int { get set }
   var result: Bool { get }

   func attendance() -> String
   func markssecured() -> String

}

protocol classb: classa {

   var present: Bool { get set }
   var subject: String { get set }
   var stname: String { get set }

}

class classc: classb {
   var marks = 96
   let result = true
   var present = false
   var subject = "Swift Protocols"
   var stname = "Protocols"

   func attendance() -> String {
      return "The \(stname) has secured 99% attendance"
   }

   func markssecured() -> String {
      return "\(stname) has scored \(marks)"
   }
}

let studdet = classc()
studdet.stname = "Swift"
studdet.marks = 98
studdet.markssecured()

println(studdet.marks)
println(studdet.result)
println(studdet.present)
println(studdet.subject)
println(studdet.stname)
```
