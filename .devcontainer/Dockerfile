FROM ubuntu:latest

ARG USER=user
ARG GROUP=$USER
ARG UID=1000
ARG GID=$UID
ARG PASSWORD=pass

# Create a new group
RUN userdel ubuntu &&\
    groupadd -o --gid ${GID} ${GROUP} &&\
    useradd -o -ms /bin/bash --uid ${UID} --gid ${GID} ${USER} &&\
    echo "$USER:$PASSWORD" | chpasswd &&\
    mkdir -p /home/${USER}/project &&\
    chown $USER:$USER /home/${USER}/project

RUN apt update && apt install sudo -y && usermod -aG sudo ${USER}

# Uncomment below if you do not want password prompt.
# RUN echo "$USER ALL=(ALL:ALL) NOPASSWD: ALL" | tee /etc/sudoers.d/$USER

# Set the working directory
WORKDIR /home/${USER}/project
