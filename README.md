1. AMQP (Advanced Message Queuing Protocol):
- AMQP is an open standard application layer protocol for message-oriented middleware
- It enables different applications to communicate with each other reliably and securely
- It's particularly useful for distributed systems where different components need to exchange messages
- We use it through the crosstown_bus library to handle message passing between different parts of your system

2. Let's break down the connection string amqp://guest:guest@localhost:5672:
- guest:guest:
    - The first guest is the username
    - The second guest is the password
    - These are the default credentials for RabbitMQ (a popular AMQP broker)
    - In a production environment, we would typically use more secure credentials
- localhost:5672:
    - localhost means the AMQP broker (like RabbitMQ) is running on the same machine as your application
    - 5672 is the default port number for AMQP
    - If we were connecting to a remote message broker, we would replace localhost with the actual server address