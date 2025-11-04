The Model-View-Controller system is a pattern where we can organize our software into 3 categories:

**Model**: Responsible for presenting information and the business logic of the application. It handles data management, database interaction, and provides an interface to access and modify stored data.

**View**: Responsible for presenting information to the user in a clear and organized manner.

**Controller**: Acts as an intermediary between the model and the view, managing communication and coordinating actions. It processes input, interacts with the model to make changes, and updates the view as needed.

The MVC pattern promotes separation of responsibilities and facilitates maintainability, scalability, and code reusability in software applications.



## MVC to Clean MVC

Clean architecture, also known as hexagonal architecture, concentric layers, or the "onion" approach, is based on the idea of separating the most essential and high-level aspects of business logic (business rules) from the less essential and low-level details (user interface, databases, frameworks, etc.).

We can take the MVC pattern as a starting point and adapt it to a clean architecture as follows:

1.  **Entities (Core of clean architecture)**: These would be equivalent to Models in MVC. They are the classes that contain high-level business rules and don't depend on any other layer.
    
2.  **Use Cases**: This is where high-level business rules are applied to the entities. In MVC, this could be part of what a Controller does, although in clean architecture, this logic would remain separate and pure, without mixing it with user interface logic or data access logic.
    
3.  **Controllers and Presenters**: This would be an expansion of the Controller's role in MVC. The Controller handles user input, which it uses to interact with Use Cases. Then, the Presenter receives the results from Use Cases and transforms them into a form suitable for the View.
    
4.  **View**: Similar to the View in MVC, this component is responsible for presenting information to the user. However, in clean architecture, the View would be even thinner and less intelligent, with most of the presentation logic handled by the Presenter.
    
5.  **Infrastructure Layer**: This layer has no direct equivalent in MVC and handles low-level details such as database access, networking, and other operations that don't directly relate to business rules. In clean architecture, dependencies always point inward, meaning that higher-level layers don't depend on this infrastructure layer.

The goal of clean architecture is to make the system more maintainable, flexible, and scalable, and less dependent on specific infrastructure details, frameworks, or user interfaces.