# Inheritance/Extension
* Both languages are fundamentally statically typed class-based OO languages with single inheritance. Furthermore, Swift includes the normal set of features that Java has including.
* Swift classes don't inherit from a base object class. However, Swift supports more features like Extension which Java doesn't support.The only way in java for utilizing extension is using static method.

# Inheritance
* Java

```Java
class Calculation {
   int z;

   public void addition(int x, int y) {
      z = x + y;
      System.out.println("The sum of the given numbers:"+z);
   }

   public void Subtraction(int x, int y) {
      z = x - y;
      System.out.println("The difference between the given numbers:"+z);
   }
}

public class My_Calculation extends Calculation {
   public void multiplication(int x, int y) {
      z = x * y;
      System.out.println("The product of the given numbers:"+z);
   }

   public static void main(String args[]) {
      int a = 20, b = 10;
      My_Calculation demo = new My_Calculation();
      demo.addition(a, b);
      demo.Subtraction(a, b);
      demo.multiplication(a, b);
   }
}
```
* Swift

```Swift

class Vehicle {
    var currentSpeed = 0.0
    var description: String {
        return "traveling at \(currentSpeed) miles per hour"
    }
    func makeNoise() {
        // do nothing - an arbitrary vehicle doesn't necessarily make a noise
    }
}

class Bicycle: Vehicle {
    var hasBasket = false
}

let bicycle = Bicycle()
bicycle.hasBasket = true

bicycle.currentSpeed = 15.0
print("Bicycle: \(bicycle.description)")
// Bicycle: traveling at 15.0 miles per hour
```
# Extension
 #### Swift Extension Functionalities
  * Adding computed properties and computed type properties.
  * Defining instance and type methods.
  * Providing new initializers.
  * Defining subscripts.
  * Defining and using new nested types.
  * Making an existing type conform to a protocol.

 #### Code example

```Swift

 extension Int {
   var add: Int {return self + 100 }
   var sub: Int { return self - 10 }
   var mul: Int { return self * 10 }
   var div: Int { return self / 5 }
}

let addition = 3.add
println("Addition is \(addition)")

let subtraction = 120.sub
println("Subtraction is \(subtraction)")

let multiplication = 39.mul
println("Multiplication is \(multiplication)")

let division = 55.div
println("Division is \(division)")

let mix = 30.add + 34.sub
println("Mixed Type is \(mix)")

 ```
