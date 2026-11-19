# HTTPS SSL Configuration

## Project Overview

This project is part of the ALU Webstack curriculum. It focuses on configuring HTTPS, SSL termination, DNS records, and HTTP-to-HTTPS redirection using **HAProxy**.

The main objective is to secure web traffic and ensure that users can access the web servers through an encrypted HTTPS connection.

## Learning Objectives

- Understand DNS records and domain name resolution.
- Configure DNS A records for web servers and load balancers.
- Understand SSL certificates and HTTPS.
- Configure HAProxy for SSL termination.
- Redirect HTTP traffic to HTTPS using a 301 status code.
- Improve website security through encrypted connections.

## Project Tasks

### Task 0: World Wide Web

**File:** `0-world_wide_web`

A Bash script that displays information about the DNS records of specified subdomains.

It supports:
- Displaying all configured subdomains.
- Checking an individual subdomain.
- Identifying DNS record types and their destinations.

**Usage:**

```bash
./0-world_wide_web liberytech.tech
```

To check one subdomain:

```bash
./0-world_wide_web liberytech.tech www
```

### Task 1: HAProxy SSL Termination

**File:** `1-haproxy_ssl_termination`

Configure HAProxy to terminate SSL connections using an SSL certificate generated with Certbot.

The configuration:
- Listens for HTTPS traffic on port 443.
- Uses an SSL certificate.
- Forwards requests to the backend web servers.
- Distributes traffic between the web servers.

### Task 2: Redirect HTTP to HTTPS

**File:** `2-redirect_http_to_https`

Configure HAProxy to redirect HTTP traffic to HTTPS.

The configuration:
- Listens for HTTP traffic on port 80.
- Redirects HTTP requests to HTTPS.
- Uses a permanent 301 redirect.
- Forwards secure requests to the backend web servers.

## DNS Configuration

The following DNS A records are configured:

| Subdomain | IP Address |
|---|---|
| www | 18.170.99.14 |
| lb-01 | 18.170.99.14 |
| web-01 | 18.171.210.130 |
| web-02 | 35.176.93.193 |

## Technologies Used

- Linux (Ubuntu)
- Bash scripting
- DNS
- HAProxy
- Certbot
- SSL/TLS
- Git and GitHub

## Repository Structure

```text
alu-webstack/
└── https_ssl/
    ├── 0-world_wide_web
    ├── 1-haproxy_ssl_termination
    ├── 2-redirect_http_to_https
    └── README.md
```

## Author

**Kayitare Libery**

ALU – Webstack Project
