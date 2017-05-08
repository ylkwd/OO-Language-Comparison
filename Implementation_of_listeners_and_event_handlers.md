# Java

In Java, event listeners represent the interfaces responsible to handle events. Common used event listeners are ActionListener, MouseListener, FocusListener and so on.

Following is showing one example of Implementation of ActionEvent for selecting different Checker board size.
```JAVA
@FXML
public void selectSize(ActionEvent event) {
    MenuItem menuItem = (MenuItem)(event.getSource());
    switch(menuItem.getId()) {
        case "16 x 16":
            numRows = 16;
            numCols = 16;
            break;
        case "10 x 10":
            numRows = 10;
            numCols = 10;
            break;
        case "8 x 8":
            numRows = 8;
            numCols = 8;
            break;
        case "3 x 3":
            numRows = 3;
            numCols = 3;
            break;
        default:
            setDefaultRowsCols();
    }
    renderBoard();
}
```
Following is showing one example of applying ChangeListener with renderBoard() function inside when every time the board is resizing, the width and height Property will trigger the listeners.
```JAVA
public void ready(Stage stage, Scene scene) {
       this.stage = stage;
       this.scene = scene;

       ChangeListener<Number> listener = (ObservableValue<? extends Number> observable, Number oldValue, final Number newValue) -> {
           renderBoard();
       };

       scene.widthProperty().addListener(listener);
       scene.heightProperty().addListener(listener);



       renderBoard();
   }
```
# Swift
In Swift, ActionEvent is applied by using IBOutlet and IBAction associated with UI elements residing in Main storyBoard. Following is showing how to utilize IBOutlet and IBAction to achieve what event listeners does in Java

``` Swift
import UIKit

class ViewController: UIViewController {
    //create a variable called message associated with a label UI element //in the main storyBoard using IBOutlet
    @IBOutlet weak var message: UILabel!
    override func viewDidLoad() {
        super.viewDidLoad()
        message.text = "😁"
        // Do any additional setup after loading the view, typically from a nib.
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }

    //Set a UI button in the main storyBoard with IBAction that modify the text of UILabel message
    @IBAction func notify(_ sender: UIButton) {
        message.text = "You have been notified!"    
    }
    //Set a UI button with IBAction that set text of UILabel message to empty String
    @IBAction func clear(_ sender: UIButton) {
        message.text = ""  
    }


}
```
