FROM node:16-alpine

WORKDIR /usr/app

COPY package*.json ./

RUN npm install

# Copy the rest of the application code
COPY . .

# Set the backend URL for the React application
ENV REACT_APP_BACKEND_URL=http://localhost:8080

# Build the React application
RUN npm run build

# Install 'serve' globally to serve the built app
RUN npm install -g serve

# Expose port 5000
EXPOSE 5000

# Command to serve the built app
CMD ["serve", "-s", "-l", "5000", "build"]
