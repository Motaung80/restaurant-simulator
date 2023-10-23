# Design Patterns for the Kitchen:
## Chain of Responsibility Pattern:
![cha](https://github.com/Motaung80/restaurant-simulator/assets/86393854/043a03c1-d7b6-438a-9437-4feffc2cec6f)
Use Case: Handling different stages of food preparation.
Components: Head Chef, Fry Cook, other specific chefs.
Description: Each chef represents a link in the chain. When an order comes in, it can be passed down the chain. Each chef performs their specific operation on the dish. If a chef can't handle a particular task, it's passed on to the next chef in the line. The order finally reaches the head chef for plating.

## Observer Pattern:
![Obser](https://github.com/Motaung80/restaurant-simulator/assets/86393854/1c8dc7b6-c973-4dce-bfcb-fb959600850a)
Use Case: Notifying the waiter when the order is ready.
Components: Kitchen (subject), Waiters (observers).
Description: When an order is ready, the kitchen notifies the waiter associated with that order. Each waiter can observe multiple orders, and the kitchen will have a mechanism to notify the right waiter when an order is done.

## Strategy Pattern:

Use Case: Different methods of preparation (e.g., grilled vs fried).
Components: Preparation Strategy Interface, Grilling Strategy, Frying Strategy, etc.
Description: The order will specify the preparation strategy to use, and the chefs can switch between these strategies on-the-fly to prepare the dish.

## Factory Pattern:
![Fact](https://github.com/Motaung80/restaurant-simulator/assets/86393854/5571c4ab-0f05-44c5-b22e-ab9f38e13328)
Use Case: Creating dishes based on the Build-Your-Own choices.
Components: DishFactory, Various Dish Types.
Description: Given a set of choices by the customer, the DishFactory will create and return the correct dish type, which then gets processed by the kitchen.

## Command Pattern:

![Comm](https://github.com/Motaung80/restaurant-simulator/assets/86393854/61bd283b-2e77-4b5b-a125-2b02abd6435c)
Use Case: Waiters passing orders to the kitchen.
Components: OrderCommand, Waiter, Kitchen Receiver.
Description: When a waiter gets an order, they create an OrderCommand with the details and pass it to the kitchen. The kitchen, acting as the receiver, will then execute the command, preparing the order accordingly.
Relationships:

### Kitchen and Floor:

The floor (waiters, specifically) acts as the initiator for the kitchen. The floor generates orders based on customer requests, and these orders are then processed by the kitchen.
The kitchen and floor have a two-way communication system. The floor sends order commands to the kitchen, and the kitchen sends notifications back to the floor (waiters) when orders are ready.
Chefs within the Kitchen:

Chefs work collaboratively, relying on the Chain of Responsibility pattern. They are aware of the next chef in the chain to pass the order to.
The head chef acts as the final point in the preparation process, ensuring the dish meets quality standards before signaling it's ready.

### Kitchen and Orders:

Orders are processed using a combination of the Strategy, Factory, and Command patterns. The exact flow and components involved depend on the specific order details.
Orders dictate how the kitchen functions. The type of dish, method of preparation, and other specifics guide the chefs and systems in the kitchen.
