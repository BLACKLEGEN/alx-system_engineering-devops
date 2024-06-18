# 0x16. API Advanced

This project focuses on interacting with the Reddit API to retrieve data related to subreddits. The goal is to practice API calls, JSON parsing, recursion, and handling pagination.

## Learning Objectives

By the end of this project, you should be able to:

- Read API documentation to find the required endpoints
- Use an API with pagination
- Parse JSON results from an API
- Make recursive API calls
- Sort a dictionary by value

## Project Requirements

- **Editors Allowed**: vi, vim, emacs
- **Python Version**: Python 3.4.3
- **Style Guide**: PEP 8
- **Modules**: Use the `requests` module for HTTP requests
- **Documentation**: All modules should have documentation
- **Executable Files**: All files must be executable
- **Mandatory File**: README.md file at the root of the project

## Tasks

### Task 0: How Many Subs?

Write a function that queries the Reddit API and returns the number of subscribers for a given subreddit. If an invalid subreddit is given, return 0.

- **Prototype**: `def number_of_subscribers(subreddit)`
- **Requirements**:
  - Return 0 if the subreddit is invalid.
  - Avoid following redirects for invalid subreddits.

**Example**:
```bash
$ python3 0-main.py programming
756024
$ python3 0-main.py this_is_a_fake_subreddit
0
```

### Task 1: Top Ten

Write a function that queries the Reddit API and prints the titles of the first 10 hot posts for a given subreddit. If the subreddit is invalid, print `None`.

### AUTHOR
NSANZIMANA RUGWIRO Dominique Parfait