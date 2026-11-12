FROM ubuntu
WORKDIR /usr/src/app
RUN apt-get update -y && apt-get install -y curl
RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash -
RUN apt-get install -y nodejs
RUN node -v && npm -v
COPY package* .
COPY src/ src/
COPY public/ public/ 
RUN npm install
EXPOSE 5001
RUN npm run build
RUN npm install -g serve
CMD ["serve", "-s", "-l", "5001", "build"]
 
