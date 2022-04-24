# Dockerfile for CS312 Assingment #6, Victor D. Campa
# Ansible Homework [NODE]
FROM alpine:latest

# installs
RUN apk -U add vim
RUN apk -U add openssh-server
RUN apk -U add openrc
RUN rc-update add sshd

# enable root login
# COPY sshd_config /etc/ssh/

# expose port 22
EXPOSE 22

# start sshd [enable ssh]
RUN /etc/init.d/sshd --dry-run start && touch /run/openrc/softlevel && /etc/init.d/sshd start

# looks like I need to do this manually
RUN service sshd restart



# mkdir ~/.ssh/
# create authorized_keys section in ~/.ssh/
# add chmod 600 to ~/.ssh/authorized_keys
# add chmod 600 to ~/.ssh/




# Copy the client PY file
# COPY client.py /client.py

# Run this command by default
# CMD python3 /client.py

#docker run --rm -d -p 8080:8080 707a5e9f43d7

#apk add apache2
#rc-update add apache2
#rc-update