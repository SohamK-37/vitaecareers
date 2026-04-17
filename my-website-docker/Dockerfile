# Use a lightweight Nginx image as the base
FROM nginx:alpine

# Remove the default Nginx configuration file
# This is to ensure our custom config is used
RUN rm /etc/nginx/conf.d/default.conf

# Copy your custom Nginx configuration file into the container
# This file will tell Nginx where to find your static files
COPY nginx.conf /etc/nginx/conf.d/

# Copy your entire VITAECAREER folder (containing HTML, CSS, JS)
# into the Nginx web root directory inside the container.
# Nginx typically serves from /usr/share/nginx/html by default.
# We're putting it inside a subfolder, as per our nginx.conf
COPY VITAECAREER/ /usr/share/nginx/html/VITAECAREER/

# Expose port 80, which is the default HTTP port Nginx listens on
EXPOSE 80

# The CMD command is inherited from the base Nginx image,
# which typically runs Nginx in the foreground. No need to specify here.