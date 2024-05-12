### REFLECTION MODUL 8 PUBLISHER

1. How many data messages does your publisher program send in one run?
<br>
In the provided Rust code, the main function initializes a publisher for the CrosstownBus message broker and then publishes five UserCreatedEventMessage events using the publish_event method of the publisher.

Therefore, in one run of the program, the publisher sends five data messages to the message broker.
</br>
2. What does it mean when the URL "amqp://guest:guest@localhost:5672" is used in both the publisher and subscriber programs?
<br>
This URL is commonly used to connect to a message broker using the Advanced Message Queuing Protocol (AMQP). In this URL:

"amqp://" specifies the protocol, which is AMQP.
"guest:guest" specifies the username and password for authentication. In this case, both the username and password are "guest".
"localhost" specifies the hostname or IP address of the machine where the message broker is running. "localhost" means the message broker is running on the same machine as the program.
"5672" specifies the port number on which the message broker is listening for incoming connections. This is the default port for AMQP.
When the same URL is used in both the publisher and subscriber programs, it means that both programs are connecting to the same message broker instance running on the same machine, using the same authentication credentials and port number. This ensures that the publisher can publish messages to the same message broker instance to which the subscriber is subscribed.
</br>

## Proof Rabbitmq Page
<br></br>
![img.png](static/img.png)
<br></br>

## What's Happening?
<br></br>
![img.png](static/img1.png)
<br>The image illustrates that when the publisher runs, it sends the hardcoded data from its code to the message queue. Subscribers connected to the message queue receive this data and output it in the console based on the predefined code.</br>

<br></br>
![img.png](static/img2.png)
<br>The second graph depicts a rise in message frequency over time intervals. This correlates with the execution of the cargo run command in the publisher project. Each time the publisher is executed, there's an uptick in message rates on RabbitMQ, serving its purpose as a message queue.</br>

