# Patient Journal Project

This project is a web-based **Patient Journal** system developed as part of the course **FullStack-utveckling och DevOps** during the third year of my Bachelor's in Computer Engineering at KTH. The system is built over three labs, with each lab expanding the functionality. It integrates with **HAPI FHIR** as the medical database and uses modern Full Stack and DevOps practices.

## Features
- Patient data management (observations, conditions, encounter, patient and practitioner information, and messages).
- Image handling linked to FHIR observations.
- Attribute-based search for patient records.
- Messaging between patients and practitioners.
- Authentication using **Keycloak** (final lab).
- Microservice-based architecture with Docker and Kubernetes deployment.

## Architecture Overview
The project consists of the following repositories:
1. **[Frontend Repository](https://github.com/Caraval27/CM1007-Frontend.git)**: JavaScript-based frontend.
2. **[Image Repository](https://github.com/Caraval27/CM1007-Microservice-Image.git)**: Node.js service for managing images linked to FHIR observations.
3. **[Search Repository](https://github.com/Caraval27/CM1007-Microservice-Search.git)**: Quarkus Reactive service for attribute-based search.
4. **[Health Repository](https://github.com/Caraval27/CM1007-Microservice-Health.git)**: Spring Boot service for health attributes like observations, conditions, encounters and patient/practitioner information.
5. **[Message Repository](https://github.com/Caraval27/CM1007-Microservice-Message.git)**: Spring Boot service for patient-practitioner messaging.
6. **[User Repository](https://github.com/Caraval27/CM1007-Microservice-User.git)**: Spring Boot service for user information and handling, used for labs 1 and 2 (replaced by Keycloak authentication).
7. **[Database Repository](https://github.com/Caraval27/CM1007-Database.git)**: Contains SQL schema for the MySQL database.

## Technologies Used
- **Frontend**: JavaScript, Jest (testing).
- **Backend Services**: Node.js, Spring Boot, Quarkus Reactive, Junit (test).
- **Database**: MySQL.
- **Authentication**: Keycloak (final version).
- **Message Queue**: Apache Kafka (communication between microservices _message_ and _health_).
- **Containerization**: Docker.
- **Orchestration**: CBH Cloud (KTH's Kubernetes system).
- **CI/CD**: GitHub Actions.

## Deployment
All repositories include Dockerfiles for building images. Deployment is managed using **CBH Cloud**, with CI/CD pipelines configured through GitHub Actions.
