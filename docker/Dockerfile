# Use the official nginx image from Docker Hub
FROM nginx:latest

# Set the working directory in the container
WORKDIR /sample-workflows

# Install dependencies (if needed, for a Node.js app)
# If you're serving a Node.js app directly from the container, you might still need this
# Uncomment the following lines if you need to install Node.js dependencies (for building your app first)

# Copy package.json and package-lock.json to install dependencies
# This assumes package.json is at the root of the project
COPY package*.json ./

# Install dependencies (Uncomment if you're using npm for a Node.js application)
# RUN npm install

# Build the application (uncomment if needed for a build step)
# RUN npm run build

# Copy the rest of the application files
COPY . .

# Now copy your build files to nginx directory
# Replace `./build` with your actual build directory if it's different
COPY ./build /usr/share/nginx/html

# Expose port 80 (default for nginx)
EXPOSE 80

# Command to run nginx
CMD ["nginx", "-g", "daemon off;"]
