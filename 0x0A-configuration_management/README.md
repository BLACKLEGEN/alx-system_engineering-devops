## Configuration Management Curriculum Project

### Overview

This project is a part of the Configuration Management curriculum, focusing on foundational concepts in DevOps, System Administration, Scripting, and CI/CD practices. The curriculum aims to enhance skills in managing and automating infrastructure using tools like Puppet.

### Project Details

- **SE Foundations Average:** 83.55%
- **Topic:** Configuration Management
- **Tools:** Puppet
- **Weight:** 1
- **Duration:** Started on Apr 19, 2024, and must end by Apr 25, 2024, with an auto QA review scheduled at the deadline.

### Background Context

The project stems from a real-life scenario experienced during work on an auto-remediation tool called Skynet at SlideShare. A bug in the code led to unintended consequences where a command meant for specific servers ended up affecting the entire infrastructure, causing significant downtime. This incident underscores the importance of robust configuration management practices and automation tools like Puppet.

### Resources

- **Intro to Configuration Management**
- **Puppet Resource Types:** File
- **Puppet’s Declarative Language:** Modeling Instead of Scripting
- **Puppet lint**
- **Puppet emacs mode**

### Requirements

#### General

- Operating System: Ubuntu 20.04 LTS
- File Formatting: Files must end with a new line
- README: A README.md file at the root of the project folder is mandatory
- Puppet Manifests: Must pass puppet-lint version 2.1.1 without errors, run without errors, begin with a comment explaining their purpose, and have the extension .pp

#### Versioning

- Puppet Version: Ubuntu 20.04 VM should have Puppet 5.5 preinstalled
- Puppet-lint Installation: `$ gem install puppet-lint`

### Tasks

#### 0. Create a file

- **Objective:** Use Puppet to create a file in `/tmp`.
- **Requirements:**
  - File path: `/tmp/school`
  - Permissions: 0744
  - Owner: www-data
  - Group: www-data
  - Content: "I love Puppet"

#### 1. Install a package

- **Objective:** Use Puppet to install Flask from pip3.
- **Requirements:**
  - Install Flask version 2.1.0

#### 2. Execute a command

- **Objective:** Create a Puppet manifest to kill a process named 'killmenow'.
- **Requirements:**
  - Use the exec Puppet resource
  - Utilize pkill to terminate the process

### Repository Information

- **GitHub Repository:** alx-system_engineering-devops
- **Directory:** 0x0A-configuration_management

### Copyright

Copyright © 2024 ALX, All rights reserved.

---

Feel free to extend this README with any additional information or updates as needed. Happy configuring!
