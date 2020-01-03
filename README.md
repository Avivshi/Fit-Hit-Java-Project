# Fit-Hit-Java-Project


A system that assists the user monitor and maintain his diet and training program. The project was developed in Eclipse IDE, included the use of design patterns and development of Junit test cases.

#### Architectural Pattern
The system is built according to the architectural pattern of MVC.
The following is a diagram summarizing how this architecture is implemented:
 
 ![image](https://user-images.githubusercontent.com/49638679/71702512-88d3f700-2dd8-11ea-9c2e-d099bf7cccf3.png)
 
A full breakdown of the classes can be found in the class diagram that is located in the Graphical Models folder.

#### View
The MyView class represents the View component and integrates all the UI classes by containment relationships. This class inherits the Observable class, while the UI classes implement the Observer interface and update the MyView class in events that occurred in light of user requests by the function (notifyObservers).
In addition, the MyView class also implements the Observer interface so that it could pass the user requests that came from the pages to the Controller.

#### Model
The User class represents the Model component. It contains all the information about the user that is needed for operating the system such as: his personal details, training plans and diet chosen by him and his caloric balance history. This class maintains a containment relationship with all of the other classes in the system that contain information or providing services and therefore it is the only class needed for the Model representation. In addition, this class contains methods that provide services such as: adding daily consumption / calorie expenditure, saving and reading user data for a file, etc.

#### Controller
The Controller class represents the Controller component and it contains two objects: MyView object and User object. This class implements the Observer interface and observe the two objects. Within the update method, the data is transferred between the model and the view according to the parameter Object message. This parameter contains a string / object which according to its contents the controller can tell what action should it take now. For example: user registration, data entry from a particular page, viewing a specific page, etc.

#### Graphical Models
All graphical models including: use case, class diagram and all of the sequence diagrams are attached to the Graphical Models folder.
