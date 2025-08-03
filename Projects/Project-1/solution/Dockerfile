FROM node:14.16.0-alpine3.13

# Create non-root user and group
RUN addgroup app && adduser -S -G app app

# Switch to the new user
USER app

# Set working directory
WORKDIR /app

# Copy dependency definitions
COPY package*.json .

# Install dependencies
RUN npm install

# Copy source code
COPY . .

# Set environment variable
ENV API_URL=http://api.myapp.com/

# Expose the port the app runs on
EXPOSE 3000

# Run the application
CMD ["npm", "start"]