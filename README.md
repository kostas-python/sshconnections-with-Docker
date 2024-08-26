SSH Connections Project for training perpose

Overview
This project includes a script (connect.sh) for connecting to Docker containers using SSH. It automates the process of connecting to two specific containers within a Docker network.

Prerequisites
Docker: Ensure Docker is installed and running on your machine.
SSH Access: Ensure you have SSH access configured for the Docker containers.
Setup
Clone the Repository

Clone this repository to your local machine:

bash
Copy code
git clone https://github.com/kostas-python/sshconnections-with-Docker
Navigate to the Project Directory

bash
Copy code
cd your-repo-name
Verify Docker Containers

Ensure your Docker containers are running. Use the following command to list running containers:

bash
Copy code
docker ps
Ensure container1 and any other relevant containers are listed.

Update SSH Script

Modify the connect.sh script if necessary. Ensure that the IP addresses or hostnames in the script match those of your Docker containers.

Usage
Make the Script Executable

Make sure the connect.sh script is executable:

bash
Copy code
chmod +x connect.sh
Run the Script

Execute the script to connect to the Docker containers:

bash
Copy code
./connect.sh
You will be prompted to enter the SSH password for each container.

Example connect.sh Script
The connect.sh script should look like this:

bash
Copy code
#!/bin/bash

# SSH to the first Docker container
ssh user@172.17.0.2

# SSH to the second Docker container (replace with actual IP)
ssh user@<second_container_ip>
Replace user with the appropriate SSH username and <second_container_ip> with the IP address of the second container.

Troubleshooting
Connection Issues: If you encounter connection issues, verify that the Docker containers are running and accessible. Check the container IP addresses with docker inspect.

SSH Authentication: Ensure that SSH authentication is correctly set up and that you are using the correct username and password. Consider using SSH keys for improved security.

Permissions: Ensure that your user has the necessary permissions to execute Docker commands and access the containers.

