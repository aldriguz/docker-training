# Test web app that says hello world using node.js and express.

# Linux x64
FROM node:alpine3.15

LABEL org.opencontainers.image.createdBy="Hello docker world!" \
      org.opencontainers.image.authors="Kevin Alama" \
      org.opencontainers.image.description="Simple image that returns an static message 'Hello Workd'" \
      org.opencontainers.image.licence="MIT"


# Create the app directory in the container image
RUN mkdir -p /app

# source -> target (copy the source to the target)
COPY . /app

# Set working directory context
WORKDIR /app

# Install node dependencies > node_modules
RUN npm install

# Command sent to container to execute when running the image
ENTRYPOINT [ "node", "index.js" ]
