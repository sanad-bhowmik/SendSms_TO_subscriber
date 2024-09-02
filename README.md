## Overview

The SMS Sender Project is a Java-based application designed to send SMS messages to subscribers whose information is stored in a database. This application leverages the Twilio API for SMS delivery and Spring Boot for application management and database interaction.

## Features

- **Database Integration**: Retrieves subscriber details from a configured relational database.
- **SMS Sending**: Utilizes the Twilio API to send SMS messages to the subscribers.
- **Status Logging**: Records the success or failure status of each SMS sent.
- **Error Handling**: Manages and logs errors during the SMS sending process.
- **Configurable**: Easily configurable settings for database connections and SMS gateway credentials.

## Prerequisites

- **Java Development Kit (JDK)**: Version 8 or higher.
- **Apache Maven**: For building and managing project dependencies.
- **Database**: A relational database like MySQL or PostgreSQL.

## Getting Started

### 1. Clone the Repository

Clone the project repository to your local machine using Git:

```bash
git clone https://github.com/sanad-bhowmik/SendSms_TO_subscriber.git
cd sms-sender-project
```

### 2. Configure the Application

#### Database Configuration

Update the database settings in `src/main/resources/application.properties` to connect to your database:

- `spring.datasource.url`: JDBC URL for your database.
- `spring.datasource.username`: Your database username.
- `spring.datasource.password`: Your database password.

### 3. Build the Project

Compile and package the application using Maven:

```bash
mvn clean package
```

### 4. Run the Application

Execute the packaged application with the following command:

```bash
java -jar target/sms-sender-project-1.0.jar
```

## Code Structure

- **Main Application**: The entry point for the Spring Boot application.
- **SMS Service**: Service responsible for sending SMS messages via the Twilio API.
- **Subscriber Entity**: Represents subscriber data in the database.
- **Subscriber Repository**: Interface for database operations on the Subscriber entity.
- **SMS Sender Service**: Service that retrieves subscribers and sends SMS messages.
- **Application Runner**: Component that triggers SMS sending on application startup.

## Dependencies

Ensure the following dependencies are included in your Maven `pom.xml`:

- Spring Boot Starter Data JPA
- Spring Boot Starter Web
- Twilio SDK
- MySQL Connector (or other relevant database connector)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For any questions or issues, please reach out to [sanadbhowmik93@gmail.com](mailto:sanadbhowmik93@gmail.com).