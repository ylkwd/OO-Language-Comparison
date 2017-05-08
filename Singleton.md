# What is Singleton?
 Singleton pattern is a software design pattern that restricts the instantiation of a class and limits the number of object created at runtime to one object.
# Why to use?
 * It is very useful when just one object is needed. We don't have to repeatedly recreate every single object when we just want using the same object at once.
 * Singleton Implementation may also use lazy initialization, where the instance is created when the static method is first invoked.
 * Allow multiple instances in the future without affecting a singleton class’s clients
 * Provide a global point of access to the object

# When to use?
 Using Singleton pattern when to use shared resources.

# How to use?

* ## Singleton in Java
```Java
public final class Singleton {
    private static final Singleton INSTANCE = new Singleton();

    private Singleton() {}

    public static Singleton getInstance() {
        return INSTANCE;
    }
}
```
* ## Singleton in Swift

```Swift
class Trip {

    var photos = Array<TripPhoto>()
    //create a static constant called sharedInstance with a private initializer.
    static let sharedInstance = Trip(fileName: "photos")

    fileprivate init(fileName:String) {
        loadFromJSONFileInBundle(fileName: fileName)
    }
    .
    .
    .
}

class AlbumViewController: UIViewController, UICollectionViewDelegate, UICollectionViewDataSource {

    //when we want to get all the trip photos, we simply call static member sharedInstance to get all we want.
    let trip = Trip.sharedInstance

    override func viewDidLoad() {
        super.viewDidLoad()

        // Do any additional setup after loading the view.
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }

    func numberOfSections(in collectionView: UICollectionView) -> Int {
        return 1;
    }

    func collectionView(_ collectionView: UICollectionView, numberOfItemsInSection section: Int) -> Int {
        return trip.photos.count
    }


}
```
* ## Singleton in thread-safe case
```Java

public class ASingleton{

	private static ASingleton instance= null;
	private static Object mutex= new Object();
	private ASingleton(){
	}

	public static ASingleton getInstance(){
		if(instance==null){
			synchronized (mutex){
				if(instance==null) instance= new ASingleton();
			}
		}
		return instance;
	}

}
```

* ## Singleton in Lazy initialization case
```Java
public final class Singleton {
    private static volatile Singleton instance = null;

    private Singleton() {}

    public static Singleton getInstance() {
        if (instance == null) {
            synchronized(Singleton.class) {
                if (instance == null) {
                    instance = new Singleton();
                }
            }
        }
        return instance;
    }
}
```
