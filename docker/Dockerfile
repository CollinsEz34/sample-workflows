# Use official Node.js image from Docker Hub
FROM node:16

# Set the working directory in the container (this will be inside the container)
WORKDIR /sample-workflows

# Copy package.json and package-lock.json to install dependencies
# This assumes package.json is at the root of the project, adjust as necessary
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files (including source code)
COPY . .

# Expose port (default for Node.js app)
EXPOSE 3000

# Command to run the app
CMD ["npm", "start"]
