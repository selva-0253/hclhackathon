# Use an official Node.js runtime as the base image
FROM node:18-alpine

# Create app directory
WORKDIR /app

COPY package.json package-lock.json* ./
RUN npm ci --only=production || npm install --production

# Copy the rest of the application source
COPY . .

# Expose the application's port
EXPOSE 3001

# Start the server
CMD ["node", "src/index.js"]
