# Hello World Application

This is a simple "Hello World" application designed for deployment on Google Cloud Run. The application serves a static HTML page with basic styling and interactivity.

## Project Structure

```
hello-world-app
├── public
│   ├── index.html       # Main HTML file
│   ├── css
│   │   └── style.css    # Styles for the application
│   └── js
│       └── app.js       # JavaScript for interactivity
├── server.js            # Entry point for the Express server
├── package.json         # npm configuration file
├── Dockerfile           # Instructions for building the Docker image
├── .dockerignore        # Files to ignore when building the Docker image
└── README.md            # Project documentation
```

## Getting Started

### Prerequisites

- Node.js and npm installed on your machine.
- Docker installed for building the container image.

### Installation

1. Clone the repository:

   ```
   git clone <repository-url>
   cd hello-world-app
   ```

2. Install the dependencies:

   ```
   npm install
   ```

### Running the Application Locally

To run the application locally, use the following command:

```
node server.js
```

The application will be available at `http://localhost:8080`.

### Building the Docker Image

To build the Docker image, run the following command in the project root:

```
docker build -t hello-world-app .
```

### Running the Docker Container

To run the Docker container, use the following command:

```
docker run -p 8080:8080 hello-world-app
```

### Deploying to Google Cloud Run

1. Make sure you have the Google Cloud SDK installed and authenticated.
2. Deploy the application using the following command:

   ```
   gcloud run deploy hello-world-app --image gcr.io/[PROJECT-ID]/hello-world-app --platform managed
   ```

Replace `[PROJECT-ID]` with your Google Cloud project ID.

### License

This project is licensed under the MIT License. See the LICENSE file for details.