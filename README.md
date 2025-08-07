# nginx-usecases
 What is NGINX?
NGINX is an open-source, high-performance web server that also functions as:

A reverse proxy
Load balancer
HTTP cache
Mail proxy
It is designed for high concurrency, performance, and low memory usage — making it ideal for modern DevOps and cloud environments.

Reverse Proxy
nginx-reverse-proxy
📊 NGINX vs Apache (Why DevOps Prefer NGINX)
Feature	NGINX	Apache
Architecture	Event-driven (asynchronous)	Process/thread-based
Performance	High concurrency, fast	Slower with many connections
Memory usage	Low	High
Static content	Extremely fast	Good
Config format	Simple, declarative	More flexible but complex
Use cases	Web server, reverse proxy, LB	Traditional web server
💡 DevOps Engineers often choose NGINX for its:

Lightweight footprint
Ease of automation
Docker/Kubernetes friendliness
🧰 Common DevOps Use Cases for NGINX
Use Case	Example
Web server	Serving static React/Angular apps
Reverse proxy	Forwarding requests to backend apps (Node.js, Python, Java)
Load balancer	Distributing load between multiple backend servers
SSL termination	Handling HTTPS at the edge
Caching	Reducing load on upstream services
Ingress controller (Kubernetes)	Managing traffic inside Kubernetes clusters
Rate limiting & security enforcement	Protecting APIs from abuse or bots
🛠️ Installing NGINX
🐧 On Ubuntu/Debian
sudo apt update
sudo apt install nginx -y
📦 On RHEL/CentOS
sudo yum install epel-release -y
sudo yum install nginx -y
🐳 Using Docker (Recommended for DevOps)
docker run --name nginx -p 8080:80 -d nginx
Visit: http://localhost:8080

📁 NGINX File Structure (Linux)
File/Directory	Purpose
/etc/nginx/nginx.conf	Main configuration file
/etc/nginx/sites-available/	Stores virtual host (server block) configs
/etc/nginx/sites-enabled/	Symlinks to active site configs
/var/www/html	Default web root directory
/var/log/nginx/	Contains access and error logs
🧪 Demo: Run NGINX Using Docker
Step 1: Run container
docker run --name nginx-demo -p 8080:80 -d nginx
Step 2: Test in browser
Visit: http://localhost:8080
You should see the Welcome to NGINX page.

Step 3: View Logs
docker logs nginx-demo
Step 4: Clean up
docker stop nginx-demo
docker rm nginx-demo
🎯 Summary
NGINX is a lightweight, high-performance web server and reverse proxy.
Widely used in DevOps for load balancing, SSL termination, and as a reverse proxy.
Easy to install via Linux package managers or Docker.
Supports modular configuration — great for automation and CI/CD.
