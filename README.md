![Head](https://github.com/Motaung80/restaurant-simulator/assets/86393854/06a88a85-5435-465f-9d93-976b6f3c631f)

# restaurant-simulator
A restaurant is a chaotic ensemble of various processes happening at the same time (Multithreading is not required) to result in the production and sale of food to customers. These processes can be small, from being seated at a table, to massive processes such as the cooking of food at various workstations and being passed between chefs.

5.1 The Floor:
#1. Observer Pattern:

Use the Observer pattern to manage customer expectations and satisfaction. Customers, waiters, and managers can be observers, and the restaurant can notify them about events such as order completion, table availability, or complaints.
Command Pattern:

Apply the Command pattern for handling customer orders. Waiters can act as command invokers, and orders can be encapsulated as command objects, allowing you to queue, execute, and undo orders.
