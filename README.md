# RSS Aggregator App (rssagg)

## Overview

Welcome to RSS Aggregator, a lightweight and efficient RSS feed aggregator written in Go. This application allows you to easily manage, add, remove, and prioritize your RSS feeds. With seamless integration of PostgreSQL for storing user data and Go's concurrent programming model for efficient feed fetching, RSS Aggregator ensures a responsive and reliable experience.

## Features

- **User-friendly Interface:** Intuitive interface for adding, removing, and prioritizing RSS feeds.
  
- **Fast and Efficient:** Utilizes Go's concurrent programming model for efficient feed fetching, ensuring optimal performance.

- **Database Integration:** PostgreSQL is used for storing user data, providing faster response times and data persistence.

- **Dockerized:** The application is containerized using Docker, making deployment and scalability straightforward.

- **CI/CD Integration:** Robust CI/CD pipeline integrated with testing, linting, styling, and security checks for reliable and secure code delivery.

- **Kubernetes Ready:** Included Kubernetes configuration files for easy deployment and management in a containerized environment.

## Technologies Used

- **Go (Golang):** Main programming language for building the application.
  
- **PostgreSQL:** Database system used for storing user data.

- **Docker:** Containerization for easy deployment and scalability.

- **Postman:** Used for testing API endpoints during development.

- **Go-Chi:** Lightweight and flexible HTTP router for Go.

## Build and Deployment

### Prerequisites

- Go installed on your local machine.
  
- Docker installed for containerization.
  
- PostgreSQL database set up and configured.

### Building the Application

1. Clone the repository:
   ```bash
   git clone [repository_url]
   cd rssagg
   ```

2. Build the application:
   ```bash
   go build -o rssagg
   ```
3. Add .env file
   ```bash
   PORT=${PORT}
   DB_URL=${DBURL}
   ```
4. Run the application:
   ```bash
   ./rssagg
   ```

### Docker

Build a Docker image:
```bash
docker build -t rssagg:latest .
```

Run the Docker container:
```bash
docker run -p 8080:8080 -e DB_URL=[your_database_url] -e PORT=[your_port]  rssagg:latest
```

### Kubernetes Deployment

work in progress :)

## CI/CD Pipeline

The CI/CD pipeline is configured to execute the following steps:

1. **Linting:** Ensure clean and consistent code using linting tools.
  
2. **Testing:** Run unit tests to verify the functionality of the application.
  
3. **Styling:** Check code styling and formatting for adherence to best practices.
  
4. **Security:** Scan for potential security vulnerabilities in the code.
  
5. **Build Docker Image:** Build a Docker image for containerization.
  
6. **Deploy to Cloud Run on Google Cloud:** Deploy the application to a serverless Cloud Run API of GCP.

## Contributing

We welcome contributions! Feel free to submit issues, feature requests, or pull requests. 


## Contact

For any questions or support, please contact [vishalsonyabcl@gmail.com].

Happy RSS Aggregating!
