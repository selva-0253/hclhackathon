# Use official Node.js image
FROM node:18-alpine

# Create app directory
WORKDIR /app

# Copy package files (if they exist)
COPY package*.json ./

# Install dependencies
RUN npm install --production || true

# Copy the rest of the app
COPY . .

# Expose the app port
EXPOSE 3000

# Start the server
CMD ["node", "src/index.js"]
