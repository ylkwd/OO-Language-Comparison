# Reflection
What reflection abilities are supported?
How is reflection used?


## Java:
Reflection is commonly used by programs which require the ability to examine or modify the runtime behavior of applications running in the Java virtual machine. This is a relatively advanced feature and should be used only by developers who have a strong grasp of the fundamentals of the language. With that caveat in mind, reflection is a powerful technique and can enable applications to perform operations which would otherwise be impossible.
```Java
  Method[] methods = MyObject.class.getMethods();

	for(Method method : methods){
	    System.out.println("method = " + method.getName());
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
Reflection in Swift is easy using the struct Mirror, with it we can inspect the names and types of properties in an instance of a struct or an instance of a class (soon you’ll see why it was important to bold the words).
```Swift
import Foundation.NSURL

public class Store {
    let storesToDisk: Bool = true
}
public class BookmarkStore: Store {
    let itemCount: Int = 10
}
public struct Bookmark {
   enum Group {
      case Tech
      case News
   }
   private let store = {
       return BookmarkStore()
   }()
   let title: String?
   let url: NSURL
   let keywords: [String]
   let group: Group
}

let aBookmark = Bookmark(title: "Appventure", url: NSURL(string: "appventure.me")!, keywords: ["Swift", "iOS", "OSX"], group: .Tech)

let aMirror = Mirror(reflecting: aBookmark)
print(aMirror)
// prints : Mirror for Bookmark

```
