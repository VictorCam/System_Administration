# Dockerfile for CS312, Benjamin Brewster, Elijah Voigt
# Simple NodeJS Hello World server
FROM alpine:latest

# installs
RUN apk -U add vim
RUN apk -U add python3
RUN apk -U add openssh-keygen
RUN apk -U add openssh
RUN apk -U add openrc
RUN apk -U add ansible
RUN apk -U add sshpass
RUN apk -U curl

# copy files over to root dir
COPY hosts.ini ~/
COPY My Test Page.html ~/
COPY webserver.yaml ~/

# generate ssh_key
RUN ssh-keygen -t rsa

# add chmod 600

# Expose the port 22
EXPOSE 22


# Copy the client PY file
# COPY client.py /client.py

# Run this command by default
# CMD python3 /client.py

#docker run --rm -d -p 8080:8080 707a5e9f43d7

#apk add apache2
#rc-update add apache2
#rc-update