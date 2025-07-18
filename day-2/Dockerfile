# Pakai Base Nginx 
FROM nginx:alpine

# Copy file dari host ke container 
COPY ./html /usr/share/nginx/html

# Jalankan di port 80 container
EXPOSE 80

# Jalankan nginx default command
CMD ["nginx", "-g", "daemon off;"]