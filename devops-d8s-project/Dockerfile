# Use lightweight nginx image
FROM nginx

# Remove default nginx html files
RUN rm -rf /usr/share/nginx/html/*

# Copy our app html to nginx folder
COPY app/index.html /usr/share/nginx/html/index.html

# Expose port 80
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]
