# AI-model-deployment_GenomeSequencing

## Aim
To develop and deploy a sophisticated and user-friendly web application capable of predicting the origin or spread location accurately based on genomic sequences. By combining robust AI/ML models, efficient backend systems, and an intuitive frontend interface, the goal is to provide a powerful tool for researchers, healthcare professionals, and enthusiasts to analyze and understand genomic data related to the COVID-19 pandemic.

## Getting Started
### Prerequisites

Make sure you have the following software installed on your local machine:

- [Docker](https://docs.docker.com/get-docker/)
- [Node.js](https://nodejs.org/) (only if you want to run the application locally without Docker)
- [Python](https://www.python.org/downloads/) (only if you want to run the application locally without Docker) 

### Running the Application with Docker

These instructions will help you run the application using Docker. If you prefer to run it locally, please skip to the "Local Development" section. The Docker files for the frontend and backend are already included in the repository and can be found in the `Frontend/` and `Backend/` directories respectively. These files are used by Docker Compose to build the images and run the containers.

- Clone this directory and move to its root using `cd AI-Model-Training-Deployment-Genome-Sequencing_Girlgenius/`
- Download the classifier model from [here](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/jewel_benny_students_iiit_ac_in/Ed6u3YVQ7h9Pjwq-Rb6JwLQB6kSKBD9VpwhktuJX2fliYw?e=cRJYtS) (The model is too large to be uploaded to GitHub) and copy it to the `Backend/` directory. This step is important as the model is required for the backend service to run.
- Build the Docker images for the frontend and backend by running `docker-compose build`
- This will create the Docker images for the frontend and backend services with the names `ai-model-training-deployment-genome-sequencing_girlgenius-frontend` and `ai-model-training-deployment-genome-sequencing_girlgenius-backend` respectively.
- After the images are successfully built, you can run the application using `docker-compose up`
- Docker Compose will start the container, and the application frontend will be accessible at the following URL: [http://localhost:3000](http://localhost:3000)
- The backend service will be running at [http://localhost:8000](http://localhost:8000)
- To stop the application and shut down the containers, press `Ctrl + C` in the terminal where Docker Compose is running.

> Note - Running Docker with `sudo` can be necessary if your user doesn't have the necessary permissions to interact with Docker.

## Local Development 

### Frontend
- Run `cd Frontend/`
- Run `npm install` to install all the dependencies to run the application.
- run `npm start` to run the app in the development mode.
- Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

> Note - If you want to build the app for production, run `npm run build` and the build will be stored in the `build/` directory. This will correctly bundle React in production mode and optimize the build for the best performance.

- The frontend is built using [React](https://reactjs.org/) and [Bootstrap](https://getbootstrap.com/).
- The console will display useful information such as the request and response data made to the backend service, and any errors that occur.

### Backend
- Run `cd Backend/`
- Download the classifier model from [here](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/jewel_benny_students_iiit_ac_in/Ed6u3YVQ7h9Pjwq-Rb6JwLQB6kSKBD9VpwhktuJX2fliYw?e=cRJYtS) (The model is too large to be uploaded to GitHub) and copy it to the `Backend/` directory. This step is important as the model is required for the backend service to run.
- Run `pip install -r requirements.txt` to install all the dependencies to run the application.
- Run `python -m uvicorn main:app --host 0.0.0.0 --port 8000` to run the backend service.
- The backend service will be running at [http://localhost:8000](http://localhost:8000)
