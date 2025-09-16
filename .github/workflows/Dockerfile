# Use the official Nginx image as a base
FROM nginx:alpine

# Install any necessary packages
RUN apk update && apk add --no-cache bash

# Remove default nginx website
RUN rm -rf /usr/share/nginx/html/*

# Copy the HTML file to the nginx directory
COPY index.html /usr/share/nginx/html/

# Create directory for images (if needed)
RUN mkdir -p /usr/share/nginx/html/images

# Copy nginx configuration (if custom configuration is needed)
# COPY nginx.conf /etc/nginx/nginx.conf

# Expose port 80
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]