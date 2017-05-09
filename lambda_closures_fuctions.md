## Lambda expressions, closures, or functions as types

### Java

- Java lambda expressions are new in Java 8, they facilitate functional programming, and simplify the development a lot.
- A Java lambda expression is thus a function which can be created without belonging to any class. 
- A lambda expression can be passed around as if it was an object and executed on demand.

```Java
//Traditional way
public class Person {

    public enum Sex {
        MALE, FEMALE
    }

    String name;
    LocalDate birthday;
    Sex gender;
    String emailAddress;

    public int getAge() {
        // ...
    }

    public void printPerson() {
        // ...
    }
}

//Using Lambda expressions
public static void printPersonsOlderThan(List<Person> roster, int age) {
    for (Person p : roster) {
        if (p.getAge() >= age) {
            p.printPerson();
        }
    }
}
```

### Swift

In Swift, there are four kinds of expressions
- Prefix expressions, it allows user to apply operators to smaller expressions.
- Binary expressions, it also allows user to apply operators to smaller expressions. 
- Primary expressions is conceptually the simplest kind of expression, it provides a way to access values.
- Postfix expressions is similar to prefix and binary expressions, it allows user to build up more complex expressions like function calls and member access. 

Evaluating an expression returns a value, causes a side effect, or both.

```Swift
let strings = numbers.map { (number) -> String in
    var number = number
    var output = ""
    repeat {
        output = digitNames[number % 10]! + output
        number /= 10
    } while number > 0
    return output
}
```



