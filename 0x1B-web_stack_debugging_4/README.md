# README

## Project Overview
This project focuses on debugging and optimizing web stack setups, specifically Nginx under high load, and addressing system limitations for user file access. By the end of the project, the web server should handle high traffic without errors, and the system should allow users to open files without hitting system limits.

### Puppet-lint Installation
```sh
$ apt-get install -y ruby
$ gem install puppet-lint -v 2.1.1
```

## Tasks

### 0. Sky is the Limit, Let's Bring That Limit Higher
**Objective**: Optimize the web server setup to handle high traffic without failed requests.

**Details**:
- **Tool**: ApacheBench (ab)
- **Initial Issue**: 943 out of 2000 requests failed.
- **Server**: Nginx/1.4.6 on localhost

**Steps**:
1. Benchmark the server:
    ```sh
    ab -c 100 -n 2000 localhost/
    ```
2. Apply the Puppet manifest:
    ```sh
    puppet apply 0-the_sky_is_the_limit_not.pp
    ```
3. Benchmark the server again to ensure zero failed requests.

**Expected Result**:
- 0 failed requests
- Improved request handling (6650.99 requests per second, mean time per request: 15.035 ms)

**File**: `0-the_sky_is_the_limit_not.pp`

### 1. User Limit
**Objective**: Adjust the OS configuration to allow the `holberton` user to open files without error messages.

**Details**:
- **Initial Issue**: `Too many open files` error when logging in as `holberton`.

**Steps**:
1. Attempt to login and open a file as `holberton`:
    ```sh
    su - holberton
    head /etc/passwd
    ```
2. Apply the Puppet manifest:
    ```sh
    puppet apply 1-user_limit.pp
    ```
3. Verify that the `holberton` user can now open files without errors.

**Expected Result**:
- Successful login and file access without errors.

**File**: `1-user_limit.pp`

## Repository Structure
- **GitHub Repository**: `alx-system_engineering-devops`
- **Project Directory**: `0x1B-web_stack_debugging_4`

### Files
- `0-the_sky_is_the_limit_not.pp`: Puppet manifest for task 0.
- `1-user_limit.pp`: Puppet manifest for task 1.

---

© 2024 ALX, All rights reserved.
