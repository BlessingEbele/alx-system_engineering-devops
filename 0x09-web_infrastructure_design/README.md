0x09. Web Infrastructure Design
Task 0 – Simple Web Stack
Overview
The goal of this task is to design a basic web infrastructure to host the website www.foobar.com using a single server. This is the most minimal deployment setup for a web application.

Infrastructure Components
1 Server

Hosts:

Nginx Web Server

Application Codebase

MySQL Database

Domain Name: www.foobar.com pointing to the server’s public IP address.

Request Flow
User types www.foobar.com in a browser.

DNS resolves the domain to the public IP of the server.

Nginx Web Server receives the request and:

Serves static files directly.

For dynamic requests, forwards them to the application code.

Application processes the request, interacts with the MySQL database if necessary, and returns the result.

Nginx sends the response back to the client browser.

Why These Components Are Added
Nginx Web Server: Handles HTTP requests, serves static content, and acts as a reverse proxy to the application.

Application Codebase: Contains the business logic and handles dynamic content generation.

MySQL Database: Stores persistent data for the application (e.g., user accounts, posts).

Issues With This Setup
Single Point of Failure (SPOF): If the server goes down, the website becomes unavailable.

Scalability Limits: One server handles everything — traffic spikes can overload it.

Security Concerns:

No firewall in place.

No HTTPS encryption.

No Monitoring: Failures or performance issues may go unnoticed.

Whiteboard Diagram
