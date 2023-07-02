
FROM golang:1.19

# Set the working directory inside the container
WORKDIR /app

# Copy the Go modules manifests
COPY go.mod go.sum ./

# Download and cache Go modules
RUN go mod download

# Copy the entire backend source code to the container
COPY . .

# Build the backend binary
RUN go build -o backend

# Expose the port that the backend will listen on
EXPOSE 8080

# Start the backend server
CMD ["./backend"]
