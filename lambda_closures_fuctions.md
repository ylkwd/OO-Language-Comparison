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
