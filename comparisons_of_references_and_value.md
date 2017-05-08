## Comparisons of references and values

### Java

- In Java, "==" is used to compare value, .equals(), compareTo(), and compare() are used to compare references

```Java

//compare value
int x = 1;
int y = 2;

if(x == y)
	System.our.print("there are the same");
else
	System.our.print("there are not the same"); //it will print this

//compare references by using .equals()
Class1 class1 = new Class1();  
Class2 class2 = new Class2(); 

if(class1.equals(class2)) {
    System.our.print("there are the same");
}

```

### Swift

- In Swift, "==" is used to compare value same as Java, but Swift uses "===" to compare references.

```Swift
var aString = "123"                                 // "123"
var bString = (aString as NSString)                 // "123"
aString == bString                                       	// true, content equality
aString === bString           								// error

var st1 = NSString(string:st)                  // "123"
var st2 = st1                                  // "123"
st1 === st2                                    // true

```