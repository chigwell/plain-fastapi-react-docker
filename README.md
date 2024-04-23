# plain-fastapi-react-docker

This project is a basic setup for a web application using FastAPI and React, containerized with Docker. The backend serves a simple API that communicates with the frontend, which displays data retrieved from the API.

## Project Structure

- `backend/`: Contains the FastAPI application.
  - `app/main.py`: Entry point for the FastAPI application.
  - `Dockerfile`: Docker configuration for building the backend image.
  - `requirements.txt`: Python dependencies required by the backend.

- `frontend/`: Contains the React application.
  - `public/index.html`: HTML template for the React application.
  - `src/`: React source files including `App.js` and `index.js`.
  - `Dockerfile`: Docker configuration for building the frontend image.
  - `package.json`: NPM dependencies and scripts for the frontend.

- `.gitignore`: Specifies intentionally untracked files to ignore.
- `docker-compose.yml`: Defines and runs multi-container Docker applications.
- `LICENSE`: The license file.
- `README.md`: Documentation about this project.

## Requirements

To run this project, you will need Docker and Docker Compose installed on your machine. Installation guides for Docker can be found [here](https://docs.docker.com/get-docker/) and for Docker Compose [here](https://docs.docker.com/compose/install/).

## Running the Application

1. **Clone the Repository**
   ```bash
   git clone https://yourrepositoryurl/plain-fastapi-react-docker.git
   cd plain-fastapi-react-docker
   ```

2. **Build and Run the Docker Containers**
   ```bash
   docker-compose up --build
   ```

   This command builds the images for the frontend and backend if they don't exist and starts the containers. The backend is available at `http://localhost:80/` and the frontend at `http://localhost:3000/`.

3. **Viewing the Application**

   Open a browser and navigate to `http://localhost:3000/` to view the React application. It should display a message fetched from the FastAPI backend.

## API Endpoints

The backend server has the following API endpoint:
- `GET /`: Returns a simple JSON `{ "Hello": "World" }`.

## Stopping the Application

To stop the application and remove containers, networks, and volumes created by `docker-compose up`, you can use:
```bash
docker-compose down -v
```

## Contributing

Contributions to this project are welcome. Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.
