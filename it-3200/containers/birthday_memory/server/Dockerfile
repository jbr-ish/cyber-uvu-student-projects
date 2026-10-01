FROM node:18-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install application dependencies, minus dev dependencies
RUN npm ci --omit=dev

# Copy the rest of the application code to the container
COPY . .

# Expose a port if your application listens on a specific port
EXPOSE 4000

# Define the command to run your application
CMD ["npm", "start"]