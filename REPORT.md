
#Introduction
Through this course I can learn how git, Jenkins, Maven, Ansible Docker and Kubernetes are collaboratively working for a CI/ CD pipeline and the logical workflow of a DevOps Project
CI/CD stands for Continuous Integration and Continuous Delivery/Deployment. It's a software development practice that automates the process of integrating code changes, testing them, and deploying them efficiently.
-	Continuous Integration (CI): Developers frequently merge their code changes into a shared repository. Automated tests and builds ensure that new code integrates smoothly without breaking existing functionality.
-	Continuous Delivery (CD): Once the code passes CI, it is automatically prepared for release. Developers can deploy updates at any time with minimal manual intervention.
-	Continuous Deployment (CD): This takes automation a step further—every validated change is deployed to production automatically, without requiring manual approval.
-	This project is aiming to create a CI/CD pipeline using DevOps tools and the continuous workflow of a pipeline



#Programming Tools 
The DevOps tools were used throughout the project to build, test, deploy and manage the application and infrastructure are:
Git: -
      For version control and source code management
Maven: -
      For building and managing project dependencies of the java application
Jenkins: -
      For automating the continuous integration (CI) and continuous delivery (CD) pipeline.
Docker: -
      For containerizing the application to ensure consistency across environments
Ansible: -
     For automating infrastructure configuration and software provisioning
Kubernetes: -
      For container orchestration, deployment, scaling, and management
Kubectl:-
      Command-line tool to interact with the Kubernetes cluster
AWS EC2: -
       Used to host and run Jenkins, Ansible, Kubernetes master and worker nodes, and Docker containers

#Implementation
CI/CD pipeline using Git, Jenkins and Maven
Setup Jenkins server
-	Launch an instance on AWS        
-	Installing Jenkins
Integrate Git with Jenkins
-	Install git on Jenkins instance
-	Install GitHub Plugin on Jenkins GUI
-	Configure Git on Jenkins GUI
-	Configure the name and path of git on jenkins
-	Manage Jenkins->Tools->git
       
Run Jenkins job to pull code from GitHub
-	Jenkins
-	New Item->source code management->git
-	Give the github repository url
-	Build now
 Integrate Maven with Jenkins
-	Set up Maven on Jenkins Server
-	Setup Environment variables
-	Install Maven plugins
-	Configure Maven and Java 
-	Extracting the tar file
-	Change the name to maven for easy access
-	Install Maven Integration plugin on Jenkins
-	Provide the path of jdk and maven
Integrating Tomcat server in CI/CD pipeline
Setup a Tomcat server
-	Setup a Linux EC2 Instance for tomcat  
-	Set up java for Tomcat
 	Change the directory and installing Tomcat
-	Extracting the downloaded file
 Changing the extracted file name for easy access
-	Start the tomcat server by executing a file
Integrate Tomcat with Jenkins
-	Install “deploy to container” plugin on Jenkins
-	Manage Jenkins-> Credentials->System->Add Credentials

                        
Create a first docker file
-	Create a Docker file               
-	Create a Docker image from the Docker file                            
Integrate Docker with Jenkins
-	Check that any other user other than ec2 and groups               
-	Add a user      
-	Add docker admin user to docker group
-	Jenkins->Manage Jenkins-> Plugins->Install “Publish over SSH”
                 
-	Manage Jenkins->System->SSH->Add
-	Hostname->Private IP address of the docker
             
                    
Jenkins job to automate CI/CD to deploy application on docker container
-	Jenkins->BuildAndDeployOnContainer
             
Integrating Ansible in CI/CD pipeline
Ansible installation
-	Launch an EC2 Instance
-	Set up a user and password
-	Install ansible 
Integrate docker with ansible
-	Adding docker host Ip to ansible hosts
-	Delete all the configurations from hosts file and add the IP of docker
-	Copy the key from ansible to docker
-	Check that is ansible can connect with all the hosts
ansible all -m ping (all – whatever hosts are in the inventory file it will try to connect to the system)

Integrate ansible with Jenkins
-	Jenkins->Manage Jenkins->System->Add SSH
-	Hostname (Private Ip of ansible)

Ansible playbook to create image and container

-	Adding ansible hosts to ansible inventory file
    
-	Checking if all the host can connect                   

Kubernetes on AWS
Setup bootstrap server for eksctl
-	Launch an Instance
-	Check the aws version and remove the older version
-	Install kubectl
-	Install eksctl
-	Create an IAM role on aws
-	Give Administratoracces
-	Usecase as ec2
-	Add that IAM role to eks_bootstrap
Setup Kubernetes using eksctl
-	Create cluster
Integrating Kubernetes in CI CD pipeline
Use deployment and service files to create and access pod
-	Regapp-deployment.yml
-	Regapp-service.yml
 Integrate Kubernetes Bootstrap server with ansible
-	Create a user
                 
-	Add that user to sudousers file
 Create ansible playbooks for deploy and service files
#Conclusion:-
This project provided hands-on-experience with implementing a complete DevOps lifecycle using industry-standards tools. By integrating Git, Maven , Jenkins, Docker, Ansible , Kubernetes and AWS , i was able to automate the process of building, deploying, and managing a java- based application. The course reinforced key DevOps principles such as continuous integration, continuous deployment and container orchestration. Faced some challenges when installing tools and also managing the time. Overcame these challenges with the help of mentors and teammates and did  research about that topic. Overall, it enhanced practical understanding of end-to-end DevOps workflows in a cloud-based environment

