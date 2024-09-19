# Use the official Go image as a build environment
FROM golang:1.20 AS builder

# Set the working directory inside the container
WORKDIR /app

# Copy go.mod and go.sum and download the dependencies
COPY go.mod go.sum ./
RUN go mod download

# Copy the source code into the container
COPY . .

# Build the application
RUN go build -o app2 ./app2.go

# Use a minimal base image
FROM alpine:3.17

# Copy the built application from the builder stage
COPY --from=builder /app/app2 /app2

# Expose port 8080
EXPOSE 8080

# Run the application
ENTRYPOINT ["/app2"]
