# 	Properties
Getters and setters...write your own or built in?

Backing variables?

Computed properties?

## Java:
To define a property in a bean class, supply public getter and setter methods. For example, the following methods define an int property called mouthWidth:
```Java
public class FaceBean {
	    private int mMouthWidth = 90;

	    public int getMouthWidth() {
	        return mMouthWidth;
	    }

	    public void setMouthWidth(int mw) {
	        mMouthWidth = mw;
	    }
	}
```
Java has no backing variables use in the property store and set
No computed property in Java

## Swift:
```Swift
class Temperature {
    var celsius: Float = 0.0
    var fahrenheit: Float {
    get {
        return (celsius * 1.8) + 32.0
        }
    set {
        celsius = (newValue - 32)/1.8
    }
    }    
}

var temp = Temperature()

temp.fahrenheit = 89
```
A Swift property does not have a corresponding instance variable, and the backing store for a property is not accessed directly. This approach avoids confusion about how the value is accessed in different contexts and simplifies the property’s declaration into a single, definitive statement. All information about the property—including its name, type, and memory management characteristics—is defined in a single location as part of the type’s definition.
In addition to stored properties, classes, structures, and enumerations can define computed properties, which do not actually store a value. Instead, they provide a getter and an optional setter to retrieve and set other properties and values indirectly.
