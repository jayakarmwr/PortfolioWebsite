# 📦 HTML Portfolio Deployment using Docker & EC2

This project demonstrates how to deploy a static HTML page using Docker on an AWS EC2 instance and make it publicly accessible via IP address. The Docker image is also pushed to Docker Hub for reuse.

---

## 🛠 Steps Performed

1. *Pushed HTML file to GitHub*
2. *Created an EC2 instance on AWS*
3. *Connect into the instance*
4. *Cloned the GitHub repository*
5. *Navigated into the project folder*
6. *Created a Dockerfile*
7. *Built a Docker image using the Dockerfile*
8. *Run the Docker container on port 80*
9. *Verified the HTML page on the browser using EC2 public IP*
10. *Tagged the Docker image with Docker Hub username*
11. *Logged into Docker Hub*
12. *Pushed the Docker image to Docker Hub*

---

## 📁 Project Structure

/CC ├── index.html └── Dockerfile

## 🐳 Dockerfile

```Dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html

🔧 Docker Commands

# Build the image
sudo docker build -t meghana018/htmlpage .

# Run the container
sudo docker run -d -p 80:80 florence8874/htmlpage

# Tag the image
sudo docker tag florence8874/htmlpage florence8874/htmlpage

# Login to Docker Hub
sudo docker login

# Push the image
sudo docker push florence8874/htmlpage

 Access the Deployed Site
http://<your-ec2-public-ip>

Docker Hub Link

👉 meghana018/htmlpage
