# Github-Actions-EKS-CICD-Cafe-Coffee

## Workflow Diagram of my Project -
![workflow-diagram](https://github.com/mdazfar2/Github-Actions-EKS-CICD-Cafe-Coffee/assets/100375390/18fc51ab-7ccc-4971-a37c-9e740b854331)

# Description 
Welcome to Github-Actions-EKS-CICD-Cafe-Coffee! This project aims to streamline the deployment pipeline for a MERN (MongoDB, Express.js, React.js, Node.js) web application using a DevOps approach. By leveraging GitHub Actions, Docker, Terraform, and SonarQube, we've crafted an automated Continuous Integration/Continuous Deployment (CI/CD) pipeline that ensures efficiency, reliability, and quality in deploying your MERN web application to Amazon Elastic Kubernetes Service (EKS).

## Key Features -

- **Automated EKS Cluster Creation**: Utilize Terraform to automate the provisioning of Amazon EKS clusters, providing a scalable and managed Kubernetes environment.
- **Dockerized Deployment**: Docker containers are used to package the MERN application, ensuring consistency across different environments and facilitating easy deployment.
- **Github Actions Integration**: Seamlessly integrate Github Actions for automating the CI/CD pipeline, enabling continuous integration, code quality checks, and deployment.
- **SonarQube Integration**: Enhance code quality and security with SonarQube static code analysis, integrated into the CI/CD pipeline for thorough code inspection.
- **Secure Secrets Management**: Safely manage sensitive information such as API keys and credentials through Github Actions secrets, ensuring secure integration with external services like SonarQube.

  ## Getting Started -

  ## Prerequisites

     1. **AWS Account:** You need an AWS account to utilize services like Amazon EKS and EC2. If you don't have an AWS account, you can [create one here](https://signin.aws.amazon.com/signin?redirect_uri=https%3A%2F%2Fconsole.aws.amazon.com%2Fconsole%2Fhome%3FhashArgs%3D%2523%26isauthcode%3Dtrue%26nc2%3Dh_ct%26src%3Dheader-signin%26state%3DhashArgsFromTB_ap-southeast-2_aacbff57e379dd11&client_id=arn%3Aaws%3Asignin%3A%3A%3Aconsole%2Fcanvas&forceMobileApp=0&code_challenge=gz0r28YwtQey_P0ZDDgYsMbdjUHsI0LNhXn3s58m1nU&code_challenge_method=SHA-256).
 
     2. **EC2 Instance with Ubuntu AMI:**
            - **Launch EC2 Instance:** Log in to your AWS Management Console and navigate to EC2. Launch an EC2 instance with Ubuntu AMI by following these steps:

         - Choose an Ubuntu AMI (Amazon Machine Image).
         - Select the instance type. For this project, choose "t2.medium" to ensure sufficient resources.
         - Configure instance details according to your requirements.
         - Add storage: Choose at least 20GB of storage to accommodate the application and dependencies.
         - Configure security group and key pair settings.
         - Review and launch the instance.
         - Connect to EC2 Instance: Once the instance is launched, connect to it using SSH or any other preferred method. This instance will serve as your development environment and may also be used to execute Terraform scripts.
       


## Now work on terminal - 
 
  - now run the script for downloading- trivy, terraform, aws, kubectl, node, java in above repo you will get the ```script``` named ```tools.sh```
 
    ```bash
    chmod +x ./tools.sh
    ./tools.sh
    ```

  - Now check the whole tools that you have download-
 
    ```bash
    trivy --version
    terraform --version
    aws --version
    kubectl version
    node -v
    java --version
    ```

    - Firstly lauch Sonarqube using this -
    
    ```bash
    docker run -d --name sonarqube -p 9000:9000 sonarqube:lts-community
    ```
  - Then use the ip with port :9000 in your browser then SonarQube start, and type username- ```admin``` and password- ```admin```.

  - Now, execute below commands one by one

    ```bash
    git clone https://github.com/mdazfar2/Github-Actions-EKS-CICD-Cafe-Coffee.git
    ```
    ```bash
    cd Github-Actions-EKS-CICD-Cafe-Coffee
    ```
 
    # Create s3 bucket using following commands 

    ```bash
    cd s3-bucket
    ```

    ```bash
    terraform init
    ```

    ```bash
    terraform fmt
    ```

    ```bash
    terraform validate
    ```

    ```bash
    terraform plan
    ```

    ```bash
    terraform apply --auto-approve
    ```

    ```bash
    cd ..
    ```

    - **Now check your S3 bucket that it is created or not**
   
  # Now create EKS Cluster-

     ```bash
     cd Eks-terraform
     terraform init
     terraform fmt
     terraform validate
     terraform plan
     terraform apply --auto-approve
     ```

## Now use the process of Github Runner in you terminal, command will get you in setting>Actions>Runners>new self hosted runners then choose linux then do all step by step


***If you encounter any hurdles or technical challenges along the way, know that I'm here to assist you every step of the journey. Feel free to reach out to me for support and guidance. You can easily connect with me through [LinkedIn](https://linkedin.com/in/md-azfar-alam), [Instagram](https://www.instagram.com/azfarxx_/) or [Discord](https://discord.com/users/877531143610708028)***

##  Looking forward to helping you succeed! ✨
     
