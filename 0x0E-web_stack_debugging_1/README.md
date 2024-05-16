### Project Name: Web Stack Debugging #1

---

#### Description:
This project focuses on debugging a misconfiguration issue with an Nginx installation on an Ubuntu container. The tasks involve identifying why Nginx isn't listening on port 80 and automating the fix through Bash scripting.

---

#### Curriculum:
- **SE Foundations**
  - Average: 82.49%
- **DevOps**
- **SysAdmin**
- **Scripting**
- **Debugging**
- **Weight: 1**

---

#### Concepts:
- Network basics
- Web stack debugging

---

#### Timeline:
- **Project Start:** May 13, 2024 6:00 AM
- **Project End:** May 17, 2024 6:00 AM
- **Checker Released:** May 15, 2024 8:24 PM
- **Auto Review:** Launching at the deadline

---

#### Requirements:
- **General:**
  - Allowed editors: vi, vim, emacs
  - Interpreted on Ubuntu 20.04 LTS
  - Files end with a new line
  - Mandatory README.md file at the root
  - Bash scripts must be executable
  - Bash scripts must pass Shellcheck without errors
  - Bash scripts must run without errors
  - First line of Bash scripts: `#!/usr/bin/env bash`
  - Second line: comment explaining script purpose
  - No use of wget

---

#### Tasks:

##### 0. Nginx likes port 80
- **Description:**
  - Identify why Nginx isn't listening on port 80 and automate the fix.
- **Requirements:**
  - Nginx must be running and listening on port 80 of all server's active IPv4 IPs
  - Bash script to configure the server accordingly

Repo:
- GitHub repository: alx-system_engineering-devops
- Directory: 0x0E-web_stack_debugging_1
- File: 0-nginx_likes_port_80

##### 1. Make it sweet and short (Advanced)
- **Description:**
  - Implement the fix from Task #0 in a concise manner.
- **Requirements:**
  - Bash script must be 5 lines long or less
  - Cannot use `;`, `&&`, or previous script
  - Service (init) must report that nginx is not running
  - Bash script to achieve the fix

Repo:
- GitHub repository: alx-system_engineering-devops
- Directory: 0x0E-web_stack_debugging_1
- File: 1-debugging_made_short

---

#### Copyright:
Copyright © 2024 ALX, All rights reserved.
