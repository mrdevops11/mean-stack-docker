# Base Image is node image version :6 
FROM node:6

# Create the parent folder where our application to be located
RUN mkdir -p /usr/src/app

# Set the working directory for the application
WORKDIR /usr/src/app

#  Copy our package.json file to the working directory
COPY package.json /usr/src/app

# Cleaning cache of Node Package Manager
RUN npm cache clean

# Install dependencies - Node Package Manager
RUN npm install

# Copy all project files to docker image
COPY . /usr/src/app

# Expose the port on which the application will run
EXPOSE 4200

# Start the NPM service
CMD ["npm", "start"]
