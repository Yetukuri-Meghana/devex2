# Step 1 – Create project folder
mkdir docker-demo
cd docker-demo

# Step 2 – Create index.html
# (Create the file with your editor – Not a terminal command)
# File: index.html
# -----------------
# <h1>Hello from Docker!</h1>
# -----------------

# Step 3 – Create Dockerfile
# File: Dockerfile
# -----------------
# FROM nginx
# COPY index.html /usr/share/nginx/html/index.html
# -----------------

# Step 4 – Build Docker image
docker build -t myweb:v1 .

# Step 5 – Run container
docker run -d -p 8080:80 myweb:v1

# Step 6 – Check running containers
docker ps

# Step 7 – Test in browser
# Open this in your browser:
# http://localhost:8080
