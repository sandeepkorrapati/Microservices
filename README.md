# Microservices

EmployeeProducer produces the employee details through its service and EmployeeConsumer consume it

Instead of hardcoding the Service URL and Posrt of EmployeeProducer in Consumer module, Use EurekaServer that registers both the services.

Incase if the location of EmployeeProducer changes, Consumer module can still consumes the service because Producer registers itself with EurekaServer and it provides the service to Consumer

Netflix Ribbon's RoundRobinRule algorithm is used to balance the load on EmployeeProducer module. Download and run producer module on different ports to create multiple instances and consume it
