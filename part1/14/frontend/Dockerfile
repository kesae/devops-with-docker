FROM ubuntu:22.04
RUN apt-get update
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt-get install -y nodejs
COPY . .
RUN npm install
ENV REACT_APP_BACKEND_URL=http://localhost:8080
RUN npm run build
EXPOSE 5000
RUN npm install -g serve
CMD serve -s -l 5000 build
