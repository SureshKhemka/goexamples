# Use an official Go runtime as a base image
FROM golang:1.21

# Set the working directory inside the container
WORKDIR /app

# Copy go.mod and go.sum files to the working directory
COPY go.mod .

# Download dependencies using go mod
RUN go mod download

# Copy the entire project to the working directory
COPY . .

# Build the Go application
RUN go build -o helloserver

# Expose the port the app runs on
EXPOSE 80

# Command to run the executable
CMD ["./helloserver"]
