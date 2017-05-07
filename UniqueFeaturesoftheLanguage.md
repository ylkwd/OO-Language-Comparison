# Unique features of the language
* **Java** has five primary features:
	1. It must be "simple, object-oriented, and familiar".
	2. It must be "robust and secure".
	3. It must be "architecture-neutral and portable".
	4. It must execute with "high performance".
	5. It must be "interpreted, threaded, and dynamic".
* **Swift** is an alternative to the Objective-C language that employs modern programming-language theory concepts and strives to present a simpler syntax. During its introduction, it was described simply as "Objective-C without the C". For the latest version **Swift 3**, *Apple* claims that it is the result of the latest research on programming languages, combined with decades of experience building *Apple* platforms. Named parameters brought forward from *Objective-C* are expressed in a clean syntax that makes APIs in **Swift** even easier to read and maintain. Memory is managed automatically, and developers do not even need to type semicolons. **Swift** has the following features to make code more expressive:
	* Closures unified with function pointers
	* Tuples and multiple return values
	* Generics
	* Fast and concise iteration over a range or collection
	* Structs that support methods, extensions, and protocols
	* Functional programming patterns, e.g., map and filter
	* Native error handling using try / catch / throw
```Swift
extension String {
	var banana : String {
		let shortName = String(characters.dropFirst(1))
		return "\(self) \(self) Bo B\(shortName) Banana Fana Fo F\(shortName)"
	}
}

let bananaName = "Jimmy".banana		// "Jimmy Jimmy Bo Bimmy Banana Fana Fo Fimmy"
```
