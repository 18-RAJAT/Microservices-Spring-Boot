# Microservices | Spring Boot 

This repository contains the design diagram for a microservices architecture built with Spring Boot. The architecture integrates various AWS services to create a scalable and maintainable solution.

## Architecture Overview
![microservices-spring-boot](https://github.com/user-attachments/assets/9c5d25cb-a3cb-44f7-a17a-b39f3a0581db)

### Components

- **Client**: The entry point for users, interacting with the system via the API Gateway.
- **API Gateway**: Manages incoming requests and routes them to the appropriate microservices.
- **Service Discovery**: Utilizes AWS Cloud Map for registering and discovering microservices.
- **Config Server**: Manages application configurations using AWS Secrets Manager.
- **Monitoring**: Monitors the health and performance of services using AWS CloudWatch.

### Services

1. **User Service** 
   - **User API**: Handles requests related to users.
   - **User DB**: Database for storing user information (AWS RDS).

2. **Order Service** 
   - **Order API**: Handles requests related to orders.
   - **Order DB**: Database for storing order information (AWS RDS).

3. **Inventory Service** 
   - **Inventory API**: Handles requests related to inventory.
   - **Inventory DB**: Database for storing inventory information (AWS RDS).

### Connections

The connections in the architecture are as follows:

- Client → API Gateway
- API Gateway → User API
- API Gateway → Order API
- API Gateway → Inventory API
- User API ↔ User DB
- Order API ↔ Order DB
- Inventory API ↔ Inventory DB
- User API ↔ Service Discovery
- Order API ↔ Service Discovery
- Inventory API ↔ Service Discovery
- User API ↔ Config Server
- Order API ↔ Config Server
- Inventory API ↔ Config Server
- User API ↔ Monitoring
- Order API ↔ Monitoring
- Inventory API ↔ Monitoring

## Conclusion

This system design presents a comprehensive microservices architecture leveraging Spring Boot and AWS services. It emphasizes modularity, scalability, and ease of maintenance, making it well-suited for modern applications that require flexibility and performance. By adopting this architecture developers can ensure efficient communication between services while facilitating future enhancements and integrations.
