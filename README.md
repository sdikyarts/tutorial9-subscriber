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

Why the total number of queue is as such 15 (like in the screenshot below)?
The publisher code sends 5 messages each time it runs. If we run the publisher program three times (5 messages × 3 runs), the subscriber would receive 15 messages in total.
<img width="1678" alt="image" src="https://github.com/user-attachments/assets/177f526e-446e-4cbd-8dd3-e5e41e932ef9" />
