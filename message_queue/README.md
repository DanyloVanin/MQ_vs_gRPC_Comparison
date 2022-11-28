# Message Queue based communication

## Resources:
- [RabbitMQ Python Tutorial](https://www.rabbitmq.com/tutorials/tutorial-one-python.html)

## Example

```sh
# Running rabbit
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.11-management

# Running Python consumer
# cd into python directory
pip3 install pika
python3 worker.py

# Running Java producer
# cd into java directory
./mvnw clean package
java -jar target/rabbitmq-tutorials.jar --spring.profiles.active=work-queues,sender
```