# 0x1A-application_server
This contains the tasks for application server

## 0. Set up development with Python

ubuntu@443172-web-01:~/AirBnB_clone_v2$ python3 -m web_flask.0-hello_route
 * Serving Flask app '0-hello_route'
 * Debug mode: off
Address already in use
Port 5000 is in use by another program. Either identify and stop that program, or start the server with a different port.
ubuntu@443172-web-01:~/AirBnB_clone_v2$ ps aux| grep port="5000"
ubuntu   2068707  0.0  0.0   6440   708 pts/5    S+   09:18   0:00 grep --color=auto port=5000
ubuntu@443172-web-01:~/AirBnB_clone_v2$ python3 -m web_flask.0-hello_route
 * Serving Flask app '0-hello_route'
 * Debug mode: off
Address already in use
Port 5000 is in use by another program. Either identify and stop that program, or start the server with a different port.

The error showed that the port 5000 was being used by another program so I had to stop the the kill the program is by its PID

### first identify the PID of program which was using the port.

sudo netstat -tulnp | grep 5000

I found that the process PID was 236662


### then It was time to kill the process

sudo kill -9 236662

