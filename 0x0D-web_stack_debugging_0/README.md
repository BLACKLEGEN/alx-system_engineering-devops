# Project: Web Stack Debugging #0

## Description

This project is part of the Web Stack Debugging series, focusing on training individuals in the art of debugging. As a Full-Stack Software Engineer, debugging skills are crucial, and this project aims to enhance those skills through practical exercises.

## Background Context

The task involves fixing a broken web stack by identifying and resolving issues manually before creating a Bash script to automate the fix. The example given requires ensuring that the server has a copy of the `/etc/passwd` file in `/tmp` and a file named `/tmp/isworking` containing the string "OK."

## Installation and Setup

To work on this project, you will need Docker installed. Follow the instructions provided below based on your operating system:

- [Mac OS](https://docs.docker.com/desktop/mac/install/)
- [Windows](https://docs.docker.com/desktop/windows/install/)
- [Ubuntu 14.04](https://docs.docker.com/engine/install/ubuntu/)
- [Ubuntu 16.04](https://docs.docker.com/engine/install/ubuntu/)

## Project Structure

- **Checker Release**: Apr 23, 2024 6:00 PM
- **Auto Review Deadline**: Apr 24, 2024 6:00 AM

## Requirements

- Editors: vi, vim, emacs
- Ubuntu 14.04 LTS environment
- Bash scripts must be executable and pass Shellcheck without errors
- Scripts should have `#!/usr/bin/env bash` as the first line and a comment explaining their purpose as the second line

## Tasks

### Task 0: Give me a page!

Fix Apache to run on the container and return a page containing "Hello Holberton" when queried at the root.

Example:

```bash
docker run -p 8080:80 -d -it holbertonschool/265-0
curl 0:8080
```

Ensure that the `curl` command returns "Hello Holberton" without any error messages.

## Repository Information

- GitHub Repository: [alx-system_engineering-devops](https://github.com/Rugwiroparfait/alx-system_engineering-devops)
- Directory: 0x0D-web_stack_debugging_0
- File: 0-give_me_a_page

## Copyright

© 2024 ALX, All rights reserved.
