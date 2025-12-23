# Voice Assistant with OpenAI's GPT-3 and IBM Watson

## Introduction
This project is a voice assistant that uses OpenAI's GPT-3 for intelligence and IBM Watson Speech Libraries for Embed for speech-to-text and text-to-speech capabilities. The application features a responsive front-end using HTML, CSS, and JavaScript, and a reliable back-end using Flask.

## Features
*   **Speech-to-Text**: Converts user voice input into text using IBM Watson.
*   **AI Intelligence**: Uses OpenAI's GPT-3 model to understand and respond to user queries.
*   **Text-to-Speech**: Converts the AI's text response back into speech using IBM Watson.
*   **Web Interface**: Interactive web-based user interface.

## Technologies Used
*   **Python (Flask)**: Backend server.
*   **OpenAI GPT-3**: Natural Language Processing.
*   **IBM Watson Speech Libraries**: Speech-to-Text and Text-to-Speech.
*   **HTML/CSS/JavaScript**: Frontend.
*   **Docker**: Containerization.

## Prerequisites
*   Docker installed on your machine.
*   Basic knowledge of Python, HTML, CSS, and JavaScript.

## Setup and Installation

1.  **Clone the repository** (if you haven't already).

2.  **Prepare Certificates**:
    Run the following commands to set up the necessary certificates:
    ```bash
    mkdir -p certs/
    cp /usr/local/share/ca-certificates/rootCA.crt certs/
    ```
    *(Note: Adjust the source path of `rootCA.crt` if it differs on your system)*

3.  **Build the Docker Image**:
    ```bash
    docker build . -t voice-chatapp-powered-by-openai
    ```

4.  **Run the Application**:
    ```bash
    docker run -p 8000:8000 voice-chatapp-powered-by-openai
    ```

## Usage
1.  Open your web browser and navigate to `http://localhost:8000` (or the URL provided by your environment).
2.  Allow the browser to access your microphone.
3.  Interact with the voice assistant by speaking or typing messages.

## Project Structure
*   `server.py`: Flask server handling routes and API endpoints.
*   `worker.py`: Helper functions for Speech-to-Text, OpenAI processing, and Text-to-Speech.
*   `Dockerfile`: Configuration for building the application container.
*   `templates/`: HTML files for the frontend.
*   `static/`: CSS and JavaScript files.

## Authors
*   Talha Siddiqui
*   Rohit Arora

© IBM Corporation. All rights reserved.
