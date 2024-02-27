# Regular Expression Project

This project is a part of the SE Foundations curriculum with an average score of 88.49%. The focus of this project is on Regular Expressions.

## Curriculum Details
- **Module:** 0x06. Regular expression
- **Project:** RegexDevOps
- **By:** Sylvain Kalache
- **Weight:** 1
- **Project Timeline:** 
  - Start: Feb 27, 2024 6:00 AM
  - End: Feb 28, 2024 6:00 AM
- **Checker Release:** Feb 27, 2024 12:00 PM
- **Auto Review:** Will be launched at the deadline

## Concepts
For this project, the main concept you'll be focusing on is Regular Expression.

## Background Context
In this project, you'll be working with regular expressions using Oniguruma, a library commonly used by Ruby for regex operations.

Here's a Ruby code snippet you'll be using to test your regular expressions:
```ruby
#!/usr/bin/env ruby
puts ARGV[0].scan(/127.0.0.[0-9]/).join
```

## Resources
Before you start, you can refer to the following resources:
- [Regular expressions - basics](#)
- [Regular expressions - advanced](#)
- [Rubular](#): A helpful tool for testing regular expressions.
- [Use a regular expression against a problem: now you have 2 problems](#)
- [Learn Regular Expressions with simple, interactive exercises](#)

## Requirements
### General
- **Allowed Editors:** vi, vim, emacs
- **Execution Environment:** Ubuntu 20.04 LTS
- **File Endings:** All files should end with a new line
- **README:** A `README.md` file at the root of the project folder is mandatory
- **Executable Scripts:** All Bash script files must be executable
- **Shebang:** The first line of all Bash scripts should be `#!/usr/bin/env ruby`
- **Oniguruma Library:** All regex must be built for the Oniguruma library

## Quiz Questions
You've completed the quiz successfully! Keep going!

## Tasks
1. **Simply matching School**
   - **Requirements:**
     - The regular expression must match "School"
     - Create a Ruby script that accepts one argument and passes it to a regular expression matching method
   - **Example:**
     ```bash
     sylvain@ubuntu$ ./0-simply_match_school.rb School | cat -e
     School$
     sylvain@ubuntu$ ./0-simply_match_school.rb "Best School" | cat -e
     School$
     sylvain@ubuntu$ ./0-simply_match_school.rb "School Best School" | cat -e
     SchoolSchool$
     sylvain@ubuntu$ ./0-simply_match_school.rb "Grace Hopper" | cat -e
     $
     ```
   - **Repo:** [GitHub - alx-system_engineering-devops/0x06-regular_expressions](https://github.com/alx-system_engineering-devops/0x06-regular_expressions)
   - **File:** `0-simply_match_school.rb`

2. **Repetition Token #0**
   - **Requirements:**
     - Find the regular expression that will match the above cases
     - Create a Ruby script that accepts one argument and passes it to a regular expression matching method
   - **Repo:** [GitHub - alx-system_engineering-devops/0x06-regular_expressions](https://github.com/alx-system_engineering-devops/0x06-regular_expressions)
   - **File:** `1-repetition_token_0.rb`

3. **Repetition Token #1**
   - **Requirements:**
     - Find the regular expression that will match the above cases
     - Create a Ruby script that accepts one argument and passes it to a regular expression matching method
   - **Repo:** [GitHub - alx-system_engineering-devops/0x06-regular_expressions](https://github.com/alx-system_engineering-devops/0x06-regular_expressions)
   - **File:** `2-repetition_token_1.rb`

4. **Repetition Token #2**
   - **Requirements:**
     - Find the regular expression that will match the above cases
     - Create a Ruby script that accepts one argument and passes it to a regular expression matching method
   - **Repo:** [GitHub - alx-system_engineering-devops/0x06-regular_expressions](https://github.com/alx-system_engineering-devops/0x06-regular_expressions)
   - **File:** `3-repetition_token_2.rb`

5. **Repetition Token #3**
   - **Requirements:**
     - Find the regular expression that will match the above cases
     - Create a Ruby script that accepts one argument and passes it to a regular expression matching method
     - Your regex should not contain square brackets
   - **File:** `4-repetition_token_3.rb`

6. **Not quite HBTN yet**
   - **Requirements:**
     - The regular expression must exactly match a string that starts with 'h', ends with 'n', and can have any single character in between
     - Create a Ruby script that accepts one argument and passes it to a regular expression matching method
   - **Example:**
     ```bash
     sylvain@ubuntu$ ./5-beginning_and_end.rb 'hn' | cat -e
     $
     sylvain@ubuntu$ ./5-beginning_and_end.rb 'hbn' | cat -e
     hbn$
     sylvain@ubuntu$ ./5-beginning_and_end.rb 'hbtn' | cat -e
     $
     sylvain@ubuntu$ ./5-beginning_and_end.rb 'h8n' | cat -e
     h8n$
     ```
   

7. **Call me maybe**
   - **Requirement:**
     - The regular expression must match a 10-digit phone number
   - **Example:**
     ```bash
     sylvain@ubuntu$ ./6-phone_number.rb 4155049898 | cat -e
     4155049898$
     sylvain@ubuntu$ ./6-phone_number.rb " 4155049898" | cat -e
     $
     sylvain@ubuntu$ ./6-phone_number.rb "415 504 9898" | cat -e
     $
     sylvain@ubuntu$ ./6-phone_number.rb "415-504-9898" | cat -e
     $
     ```
