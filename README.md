![Head](https://github.com/Motaung80/restaurant-simulator/assets/86393854/06a88a85-5435-465f-9d93-976b6f3c631f)

# restaurant-simulator
A restaurant is a chaotic ensemble of various processes happening at the same time (Multithreading is not required) to result in the production and sale of food to customers. These processes can be small, from being seated at a table, to massive processes such as the cooking of food at various workstations and being passed between chefs.

# 5.1 The Floor:
## Observer Pattern:
![Obs](https://github.com/Motaung80/restaurant-simulator/assets/86393854/20c768f8-e5d8-4ba9-9515-9cd686ffd498)
Use the Observer pattern to manage customer expectations and satisfaction. Customers, waiters, and managers can be observers, and the restaurant can notify them about events such as order completion, table availability, or complaints.

## Command Pattern:
Apply the Command pattern for handling customer orders. Waiters can act as command invokers, and orders can be encapsulated as command objects, allowing you to queue, execute, and undo orders.

## State Pattern:
Implement the State pattern for managing the state of tables and customers. Each table and customer can have different states (e.g., empty, seated, ordering), and the state pattern helps in encapsulating and transitioning between these states.

## Composite Pattern:
Use the Composite pattern for managing tables, which can be combined or split to accommodate various party sizes. Tables can be treated as composite objects with individual parts.

## Strategy Pattern:
Apply the Strategy pattern for meal preparation methods (e.g., grilled vs. fried) and customization of orders. Create different strategies for meal preparation and allow customers to select their preferred strategy when ordering.

## Chain of Responsibility Pattern:
Use the Chain of Responsibility pattern to manage customer requests and actions. For example, a request from a customer to call the waiter can be passed through a chain of handlers until it's processed.

## Memento Pattern:
Implement the Memento pattern for managing tabs where customers can pay later. Create memento objects to save and restore the state of the bill.

# 5.2 The Kitchen:
## Command Pattern:
Utilize the Command pattern for managing orders in the kitchen. Chefs can execute cooking commands, and orders can be represented as command objects that move through different stations in the kitchen.

## Observer Pattern:
Apply the Observer pattern for notifying waiters when orders are ready to be served. Chefs and kitchen staff can act as subjects that notify the waiters (observers) when dishes are prepared.

# 5.3 Additional Instructions:
## Visitor Pattern:
Use the Visitor pattern for chefs, waiters, and managers to visit tables and assess customer satisfaction. This pattern can help in adding functionality to visit tables without modifying the customer or table classes.
Additional Ideas:

### For the extended design, you can consider the following patterns:
## Decorator Pattern:
Apply the Decorator pattern to create a flexible and extensible system for the bar with various cocktails. You can dynamically add cocktail ingredients or decorations to drinks.

## Facade Pattern:
Implement the Facade pattern for managing valet service. The facade can simplify the interaction between the customer, valet, and car retrieval process.

##Singleton Pattern:
Use the Singleton pattern for managing inventory and accounting. This ensures that there's a single point of access for maintaining inventory levels and handling financial transactions.
