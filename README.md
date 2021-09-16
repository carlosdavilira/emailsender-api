# emailsender-api
- Requerements:
   Ports: 8080(application), 5432(Postgre)
   PostgreSQL
   RabbitMQ configuration - In this case was used https://www.cloudamqp.com/

  This projects is a microservice that the main objective is send and e-mail to a destination.
  The e-mail request can be performed in two cases: 
-   Synchronous: using api REST.
-   Asynchronous: using RabbintMQ message.

- Synchronous Form.
  Just use the end-point /sending-email, sending a EmailDto.

- Asynchronous Form.
  The application connects to RabbitMQ e subscribe on ms.email queue. When a message arrives in the queue and it has the EmailModel form,
the message is processed and and e-mail is send to destination configured on EmailModel. 



