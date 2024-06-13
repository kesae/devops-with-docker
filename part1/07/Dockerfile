# Start from the Ubuntu
FROM ubuntu:22.04

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.
WORKDIR /usr/src/app

# Install curl
RUN apt-get update
RUN apt-get -y install curl

# Copy the script.sh
COPY script.sh .

# Add execution permissions during the build.
RUN chmod +x script.sh

# When running docker run the command will be ./script.sh
CMD ./script.sh
