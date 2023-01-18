# RabbitMQ 

## Installation on Ubuntu
`sudo apt install rabbitmq-server`  
If you have ***nala*** installed already use `sudo nala install rabbitmq-server`.  Incase there is an issue regarding the used port, kindly check if the port is occupied by another process  
use `sudo lsof -i :25672` to see the proces running on port 25672  
kill the process using the process PID with `sudo kill <PID>`  
start the rabbitmq server with `sudo rabbitmq-server`  

