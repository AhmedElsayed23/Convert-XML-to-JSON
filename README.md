# XML to JSON Converter Service

This is a Spring Boot service that fetches XML data from a URL, converts the XML data to JSON, and then saves the JSON data to a file. The service is designed to handle multiple requests concurrently using a thread pool.

## Features

- Fetches XML data from a specified URL.
- Converts the fetched XML data to JSON.
- Saves the converted JSON data to a file with a unique name.
- Handles multiple requests concurrently using a thread pool.
- Proper error handling and logging.

## Technologies Used

- Java
- Spring Boot
- Maven

## How to Run

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Run `mvn clean install` to build the project.
4. Run `mvn spring-boot:run` to start the application.

## Code Structure

The main service class is `XmlToJsonServices`. It contains the following methods:

- `processRequests()`: This method is responsible for fetching the XML data, converting it to JSON, and saving it to a file. It runs asynchronously in a separate thread.
- `fetchXmlData(String url)`: This method fetches the XML data from the specified URL.
- `convertXmlToJson(ObjectNode dataInstance)`: This method converts the fetched XML data to JSON.
- `saveJsonDataToFile(String jsonContent, String uniqueId)`: This method saves the converted JSON data to a file with a unique name.
