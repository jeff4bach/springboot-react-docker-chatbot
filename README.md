
## Overview

This project is forked from https://github.com/vikasrajputin/springboot-react-docker-chatbot.
I only use some of the original projects for personal purposes.
The chatbot can assist users in learning more about Spring AI by answering questions and providing information based on user queries.

## Features

- **Interactive Chatbot**: Engage with a chatbot to learn more about Spring AI and how to integrate it with your Spring Boot applications.
- **Spring Boot Backend**: A robust backend powered by Spring Boot, utilizing Spring AI for processing and generating responses using the OpenAI API - https://github.com/jeff4bach/sbdocs
- **React Frontend**: A user-friendly and responsive frontend built with React, providing an intuitive interface to interact with the chatbot.


## Tech Stack

- **Backend**: 
  - Java 17
  - Spring Boot
  - Spring AI
  - OpenAI API
- **Frontend**:
  - React
  - HTML5 & CSS3
  - Axios
  - Nginx (for serving the React app)



### Project Structure

The project is organized into two main directories:

- **spring-boot-ai-chatbot/**: Contains the Spring Boot application with Spring AI integration.
- **chatbot-ui/**: Contains the React application that serves as the chatbot interface.

### Setting Up the Environment

**(Optional) Create a `.env` file in the `chatbot-ui` directory if needed**.

### Running the Applications Locally (Without Docker)

#### Frontend (React)

1. **Navigate to the `chatbot-ui/` directory**:

    ```bash
    cd chatbot-ui
    ```

2. **Install the dependencies**:

    ```bash
    npm install
    ```

3. **Start the React application**:

    ```bash
    npm start
    ```

4. **Access the frontend**: `http://localhost:3000`

### API Endpoints

The backend provides the following key API endpoints:

- **`GET /ai/chat/string`**: Accepts a `message` query parameter and returns a response generated by the AI model.
  - **Example**: `http://localhost:8080/ai/chat/string?message=Tell me about Spring AI`
  
- **`POST /ai/chat`**: Accepts a JSON body with a `message` field and returns a response generated by the AI model.
  - **Example**:
    ```json
    POST http://localhost:8080/ai/chat
    Content-Type: application/json
    
    {
      "message": "Explain how to use OpenAI with Spring Boot"
    }
    ```

## Customization

### Modifying the Frontend

- The React frontend is located in the `chatbot-ui/` directory.
- You can customize the UI by editing the components in the `src/` directory.
- Update the styling by modifying the `Chatbot.css` file.

### Modifying the Backend

- The Spring Boot backend is located in the `https://github.com/jeff4bach/sbdocs`.
- You can customize the AI responses by modifying the services and controllers in the `src/main/java` directory.

## Deployment

### Manual Deployment (Without Docker)

- **Backend**: Deploy the Spring Boot jar to a server or cloud service (e.g., AWS EC2, Heroku).
- **Frontend**: Build the React app (`npm run build`) and serve it using a web server (e.g., Nginx, Apache).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
