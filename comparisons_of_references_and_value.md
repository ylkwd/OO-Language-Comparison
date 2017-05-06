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