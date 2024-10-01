# Use a lightweight Node.js image as the base image
FROM golang:1.16-alpine

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy the the application code
COPY . .

ENV REQUEST_ORIGIN=http://localhost:3000

RUN go build

# Expose port 8080
EXPOSE 8080

# Start the application
CMD ["./server"]
