## LINUX SERVER ON AWS EC2 WITH DOCKER - NGINX DEPLOYMENT

# Objective
Deploy Nginx containers on an Ubuntu EC2 instance using Docker.

Showcasing container management.

Port mapping, and AWS security configuration.

# Technologies
- AWS EC2 (Ubuntu)
- Docker & Docker Compose
- Nginx Web Server
- Linux Command Line

# What I Did
- Launched an Ubuntu EC2 instance and connected via SSH using .pem key.
- Updated packages and installed Docker.
- Pulled the official Nginx image and ran multiple containers:
  - Container 1 → Host port 8080
  - Container 2 → Host port 8081
- Handled container name/port conflicts by stopping/removing old containers.
- Configured EC2 Security Group inbound rules to allow traffic on ports 8080 and 8081.
- Verified containers were publicly accessible in a browser.

# Sample Commands
bash
# Pull Nginx image
docker pull nginx

# Run containers
docker run -d -p 8080:80 --name web1 nginx


docker run -d -p 8081:80 --name web2 nginx

# List containers
docker ps

# Stop & remove containers
docker stop web1 web2

docker rm web1 web2


# Outcome

Successfully deployed multiple Nginx containers on a single EC2 instance.

Gained hands-on experience with Docker,Linux server management, and AWS cloud deployment.

Containers accessible via public IP for testing:


http://<http://13.222.184.218:8080

http://<http://13.222.184.218:8081


# Skills Demonstrated

· Cloud deployment (AWS EC2)

· Linux command-line proficiency

· Docker container lifecycle management

· Network port mapping & troubleshooting

· Security Group configuration
