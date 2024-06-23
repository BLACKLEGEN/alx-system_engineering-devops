# Postmortem: Outage of WordPress Website on LAMP Stack

![Outage Meme](https://i.imgflip.com/5sftje.jpg)



*When your website decides to take a nap during prime hours...*


## Issue Summary

**Duration:**  
- Start: June 21, 2024, 2:00 PM UTC
- End: June 21, 2024, 4:00 PM UTC

**Impact:**  
- The WordPress website was down, returning a 500 Internal Server Error.
- Users were unable to access the website, resulting in a complete service outage.
- Approximately 100% of users were affected as the entire website was down.

**Root Cause:**  
- A misconfiguration in the WordPress `wp-settings.php` file, where the `php` file extensions were incorrectly written as `phpp`.

## Timeline

- **2:00 PM:** Issue detected by monitoring alert indicating that the website was returning a 500 error.
- **2:05 PM:** An engineer confirmed the issue by attempting to access the website and observing the 500 Internal Server Error.
- **2:10 PM:** Initial investigation began, focusing on recent changes to the server and application configuration.
- **2:20 PM:** Checked Apache error logs, which provided clues but did not pinpoint the exact problem.
- **2:35 PM:** Assumed it was a database connection issue and restarted MySQL service; no resolution.
- **2:50 PM:** Misleading debugging path taken by checking network connectivity and firewall settings.
- **3:00 PM:** Escalated to the senior DevOps team.
- **3:15 PM:** Senior engineer used `strace` to attach to the Apache process and identified the issue as an incorrect file extension in `wp-settings.php`.
- **3:30 PM:** Executed a temporary fix by manually correcting the file extensions.
- **3:40 PM:** Created and applied a Puppet script to automate the fix across all servers.
- **4:00 PM:** Website was fully operational, and all services were restored.

## Root Cause and Resolution

**Root Cause:**  
The root cause of the outage was a misconfiguration in the `wp-settings.php` file of the WordPress installation. Specifically, the file extensions for PHP files were mistakenly written as `phpp` instead of `php`. This caused Apache to fail in processing the PHP scripts, resulting in a 500 Internal Server Error.

**Resolution:**  
The issue was resolved by using `strace` to trace system calls and identify the exact point of failure. Once the incorrect file extensions were identified, the following Puppet script was created to automate the fix:
```puppet
# Fixes bad `phpp` extensions to `php` in the WordPress file `wp-settings.php`.

exec { 'fix-wordpress':
  command => 'sed -i s/phpp/php/g /var/www/html/wp-settings.php',
  path    => '/usr/local/bin/:/bin/'
}
```
This script was applied to correct the file extensions, and the Apache service was restarted, restoring normal functionality to the website.

## Corrective and Preventative Measures

**Improvements/Fixes:**
1. **Code Review:** Implement stricter code review processes to catch such errors before deployment.
2. **Automated Testing:** Add automated tests to check for common misconfigurations in configuration files.
3. **Monitoring Enhancements:** Improve monitoring to detect similar issues faster and provide more specific error details.

**TODO List:**
1. **Patch WordPress Configuration:**
   - Verify all PHP files have correct extensions.
   - Deploy Puppet script across all environments.
2. **Enhance Monitoring:**
   - Implement more granular monitoring of Apache error logs.
   - Set up alerts for common misconfiguration patterns.
3. **Code Review Policies:**
   - Introduce mandatory peer reviews for configuration changes.
   - Use automated linters to check for syntax errors in configuration files.
4. **Automated Testing:**
   - Develop and integrate tests to validate configuration files during the CI/CD pipeline.
5. **Documentation and Training:**
   - Update documentation on common configuration pitfalls.
   - Conduct training sessions for engineers on best practices in configuration management.

By addressing these areas, we aim to prevent similar outages in the future and ensure a more robust and resilient web stack.


---

![Debugging Diagram](https://miro.medium.com/v2/resize:fit:700/format:webp/1*cXHgV1m17EkX-WThmJHIiQ.png)
*Diagram illustrating the debugging process with `strace` and Puppet*

