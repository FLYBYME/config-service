[![Moleculer](https://badgen.net/badge/Powered%20by/Moleculer/0e83cd)](https://moleculer.services)

# Config Service

## Overview
The Config Service is a microservice built using the Moleculer framework. It provides a centralized configuration management system, allowing you to store, retrieve, and manage configuration settings for your applications.

## Features
- Store and retrieve configuration settings
- Automatically load initial configurations
- RESTful API for managing configurations
- Supports NeDB as the database adapter

## Setup
1. Clone the repository:
    ```sh
    git clone <repository-url>
    cd config-service
    ```

2. Install dependencies:
    ```sh
    npm install
    ```

3. Start the service:
    ```sh
    npm run dev
    ```

## Usage
### REST API Endpoints
- **Get Configuration**
    ```http
    GET /v1/config/get/:key
    ```
    Retrieve the value of a configuration setting by its key.

- **Set Configuration**
    ```http
    POST /v1/config/set
    ```
    Set the value of a configuration setting. If the key does not exist, it will be created.

    **Request Body:**
    ```json
    {
        "key": "your-key",
        "value": "your-value"
    }
    ```

- **Get All Configurations**
    ```http
    GET /v1/config/all
    ```
    Retrieve all configuration settings.

## Configuration
You can define initial configuration settings in the service settings. These settings will be loaded when the service starts.

```javascript
settings: {
    config: {
        "your-key": "your-value",
        // ...other configurations...
    }
}
```

## License
This project is licensed under the MIT License.
