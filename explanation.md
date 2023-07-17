# IP 2 Summary

The IP 2 project at Moringa School involves Dockerizing a Node.js application. The main objective is to create lightweight and secure Docker containers for the application, ensuring optimal performance and easy deployment.

## Choice of Base Images
- Node Alpine images were chosen as the base for containers due to their small size, reducing build times and bandwidth usage.
- Alpine Linux's limited attack surface enhances security, making it a suitable choice.

## Dockerfile Directives
- Carefully selected Dockerfile directives ensure efficient container creation and operation.
- Directives used include setting the working directory, copying application code, installing dependencies, exposing ports, and defining the default command.

## Docker-compose Networking
- Docker-compose manages networking and container orchestration.
- The ports directive facilitates port mapping for external access, and a bridge network ensures secure container communication.

## Docker-compose Volume Usage
- Docker-compose volumes are used for data persistence across container restarts, preserving essential data like databases.

## Git Workflow
- The Git Feature Branch workflow is utilized for version control, enabling seamless collaboration and change tracking.

## Debugging and Maintenance
- Measures like checking Docker logs and using Docker Inspect help identify and address runtime errors.
- Image rebuilding is performed when necessary to accommodate configuration changes.

## Docker Image Tag Naming Standards
- Adopting Docker image tag naming standards, especially semantic versioning, ensures efficient organization and management of Docker images.

The successful completion of IP 2 demonstrates the effective implementation of Docker for containerizing a Node.js application, ensuring portability, security, and scalability.
