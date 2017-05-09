## Java
Java is a multi-threaded programming language which means we can develop multi-threaded program using Java.

#### To achieve multitasking using thread

 * First way of starting a thread is to put the code you want to run in the run method of a class that implements the Runnable interface, then pass it to the constructor of a Thread class.

```Java
class CodeRunner implements Runnable {

    @Override
    public void run() {
        // Loop for ten iterations.

        for(int i=0; i<10; i++) {
            System.out.println(i + " looping ...");

            // Sleep for a while
            try {
                Thread.sleep(200);
            } catch (InterruptedException e) {
                break;
            }
        }       
    }

}

public class Application {


    public static void main(String[] args) {

        CodeRunner runner = new CodeRunner();

        Thread thread = new Thread(runner);
        thread.start();
    }

}
```

* Second way of starting a thread is to extending the Thread Class.

```Java
class ThreadDemo extends Thread {
   private Thread t;
   private String threadName;

   ThreadDemo( String name) {
      threadName = name;
      System.out.println("Creating " +  threadName );
   }

   public void run() {
      System.out.println("Running " +  threadName );
      try {
         for(int i = 4; i > 0; i--) {
            System.out.println("Thread: " + threadName + ", " + i);
            // Let the thread sleep for a while.
            Thread.sleep(50);
         }
      }catch (InterruptedException e) {
         System.out.println("Thread " +  threadName + " interrupted.");
      }
      System.out.println("Thread " +  threadName + " exiting.");
   }

   public void start () {
      System.out.println("Starting " +  threadName );
      if (t == null) {
         t = new Thread (this, threadName);
         t.start ();
      }
   }
}

public class TestThread {

   public static void main(String args[]) {
      ThreadDemo T1 = new ThreadDemo( "Thread-1");
      T1.start();

      ThreadDemo T2 = new ThreadDemo( "Thread-2");
      T2.start();
   }   
}
```
## Swift
In swift 3, there is a class called DispatchQueue that manages the execution of work items. Each work item submitted to a queue is processed on a pool of threads managed by the system. One example is GCD, which is  Grand Central Dispatch (libdispatch),  probably one of the most used technologies on all Apple platforms when it comes to performance, concurrency, parallelization and threading

#### To achieve multitasking using DispatchQueue

* How to Create a concurrent queue in Swift 3
```Swift
let concurrentQueue = DispatchQueue(label: "queuename", attributes: .concurrent)
concurrentQueue.sync {
    //Stuff Here
}
```
* Swift 3: Create a serial queue
```Swift
let serialQueue = DispatchQueue(label: "queuename")
serialQueue.sync {
   //Stuff Here
}
```
* How to use Swift 3 to Get the main queue asynchronously
```Swift
DispatchQueue.main.async {
  //Stuff Here
}
```
* using Swift 3 To get one of the background threads
```Swift
DispatchQueue.global(attributes: .qosDefault).async {
  //Stuff Here
}
```

* To get one of the background thread:(Xcode 8 beta 5)

```Swift
DispatchQueue.global(qos: DispatchQoS.QoSClass.default).async {

}
DispatchQueue.global().async {
    // qos' default value is ´DispatchQoS.QoSClass.default`
}
```
