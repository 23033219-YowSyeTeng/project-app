FROM node:16

WORKDIR /app

COPY . /app

RUN npm install -g http-server

# Default command to serve the app on port 3000
CMD ["http-server", "/app", "-p", "3000"]
