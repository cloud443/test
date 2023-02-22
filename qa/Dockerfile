# Use an official Node runtime as a parent image
FROM node:14-alpine

# Set the working directory to /app
WORKDIR /app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files to the container
COPY . .

# Build the React app
RUN npm run build

# Serve the app using a lightweight HTTP server
RUN npm install -g serve
CMD serve -s build

# Expose port 5000 to the outside world
EXPOSE 5000
