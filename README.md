# Kubernetes_Deployment_Project
Real-Time Deployment on Kubernetes cluster using Jenkins, Docker and Ansible

- This project incorporates various components to streamline the building and deployment of a Docker image to a Kubernetes cluster. It starts with the developer creating a Dockerfile 
  and pushing it to GitHub. Jenkins triggers an automated pipeline upon receiving commits.
- Jenkins connects to an Ansible server via SSH to build the image based on the Dockerfile. After successful building, the image is tagged and pushed to a Docker registry like Docker 
  Hub for storage and accessibility.
- The Ansible server then establishes an SSH connection with the Kubernetes server and executes a playbook. This playbook utilizes kubectl commands to fetch the latest image from the 
  Docker registry. The Kubernetes cluster creates a container for the application, which can be accessed using the assigned IP address and port specified in the Kubernetes 
  configuration.
- By automating with Jenkins and Ansible, the workflow reduces manual intervention, minimizes errors, and boosts productivity. It enables organizations to adopt continuous integration 
  and delivery, facilitating rapid and reliable application deployment while ensuring scalability and flexibility.
