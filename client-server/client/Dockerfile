# Dockerfile for CS312, Benjamin Brewster, Elijah Voigt
# Simple NodeJS Hello World server
FROM alpine:latest

# Install curl
RUN apk -U add curl

# Install Python
RUN apk -U add python3

# Copy the client PY file
COPY client.py /client.py

# Expose the port 8080 for HTTP
EXPOSE 8080

# Run this command by default
CMD python3 /client.py

#docker run --rm -d -p 8080:8080 707a5e9f43d7