# Base Image is node image version :8 
FROM node:8

# Create the parent folder where our application to be located
RUN mkdir -p /var/www/app

# Set the working directory for the application
WORKDIR /var/www/app

#  Copy our package.json file to the working directory
COPY package.json /var/www/app

# Cleaning cache of Node Package Manager
RUN npm cache clean

# Install dependencies - Node Package Manager
RUN npm install

# Copy all project files to docker image
COPY . /var/www/app

# Expose the port on which the application will run
EXPOSE 4200

# Start the NPM service
CMD ["npm", "start"]
