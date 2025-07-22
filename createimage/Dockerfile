# Use official Node.js 14 image
FROM node:14-alpine

# Set working directory
WORKDIR /app

# Copy package files first for better caching
COPY package.json ./

# Install dependencies
RUN npm install --production

# Copy application source
COPY . .

# Expose port
EXPOSE 3000

# Start command
CMD ["node", "app.js"]
