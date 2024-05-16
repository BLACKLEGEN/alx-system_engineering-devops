# Project: HTTPS SSL Curriculum

## Description
This project focuses on implementing HTTPS SSL and HAProxy SSL termination. It covers concepts such as DNS configuration, web stack debugging, and the significance of securing website traffic.

## Background Context
The project emphasizes the importance of securing website traffic and explores the consequences of neglecting this aspect.

## Learning Objectives
By the end of this project, participants are expected to:

- Understand the roles of HTTPS SSL and its main components.
- Explain the purpose of encrypting traffic and the concept of SSL termination.
- Configure HAProxy for SSL termination.
- Demonstrate proficiency in web stack debugging.

## Resources
Participants are encouraged to read or watch the following resources:
- What is HTTPS?
- The main elements provided by SSL.
- HAProxy SSL termination on Ubuntu 16.04.
- SSL termination.
- Bash function.
- `awk` and `dig` manual or help.

## Tasks
### Task 0: World Wide Web
- Configure domain zone to point subdomains to respective IPs.
- Write a Bash script to display information about subdomains.
- Implement error handling and utilize `awk` and Bash functions.

### Task 1: HAProxy SSL Termination
- Create a certificate using certbot.
- Configure HAProxy to accept encrypted traffic for the `www` subdomain.
- Ensure HAProxy serves encrypted traffic returning the root of the web server with "Holberton School".

## Requirements
- Utilize vi, vim, or emacs as editors.
- All files should be interpreted on Ubuntu 16.04 LTS.
- End all files with a new line.
- Include a mandatory README.md file at the root of the project folder.
- All Bash script files must be executable.
- Bash scripts should pass Shellcheck (version 0.3.7) without any error.
- The first line of all Bash scripts should be `#!/usr/bin/env bash`.
- Provide a comment as the second line explaining the script's purpose.

## Quiz Questions
Complete the quiz successfully to proceed with the project.

## Servers
Configure servers as listed:

| Name           | Username | IP              | State   |
|----------------|----------|-----------------|---------|
| 443172-web-01  | ubuntu   | 100.26.222.186 | running |
| 443172-web-02  | ubuntu   | 54.236.51.195  | running |
| 443172-lb-01   | ubuntu   | 34.224.16.180  | running |

## Copyright
© 2024 ALX. All rights reserved.

---
**Note:** For detailed implementation instructions, refer to the respective task files in the project directory on the GitHub repository: `alx-system_engineering-devops/0x10-https_ssl`.
