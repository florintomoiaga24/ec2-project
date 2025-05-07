Initial configuration
- Create an EC2 (Ubuntu) instance that will host Jenkins.
- Install and configure Jenkins on this instance with the AWS EC2 plugin
- Create a GitHub repository containing:
o Ansible playbook
o Website files
Automation Pipeline in Jenkins
- Jenkins will use the AWS CLI to create a new EC2 instance on which to run the
playbook.
- Jenkins will download the Ansible playbook and websit files from the
GitHub repository and copy it to the previously created EC2 instance.
- After the instance is created, the Ansible playbook will configure this instance as follows:
o Install Docker and Docker Compose.
o Build Docker image based on the Apache image containing the Apache image and
the website files
o Run with Docker Compose a container with the previously built image
