# Use official Node.js image from Docker Hub
FROM node:16

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to install dependencies
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose port (default for Node.js app)
EXPOSE 3000

# Command to run the app
CMD ["npm", "start"]
