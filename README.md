# Calculator App

A simple calculator built using HTML, CSS, and JavaScript, served using Nginx in a Docker container.

## Steps to Run

1. Clone the repository.
2. Build the Docker image: `docker build -t calculator-app .`
3. Run the Docker container: `docker run -p 8080:80 calculator-app`
4. Access the app at `http://localhost:8080`.

## Automation
Jenkins pipeline script is in `Jenkinsfile`.
# project-app
