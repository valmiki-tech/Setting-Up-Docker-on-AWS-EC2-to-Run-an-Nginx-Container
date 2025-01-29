# 🚀 Setting Up Docker on AWS EC2 to Run an Nginx Container
<h1>Task-1</h1>
#Prerequisites

An AWS account

Basic knowledge of EC2 instances and SSH connections

Installed AWS CLI (optional)

Docker commands

<h1>Task-2</h1>

 • Log in to the AWS Management Console 

 • In the AWS console home, click EC2 to open the EC2 dashboard.

![image-1](https://github.com/user-attachments/assets/0f23648c-67ba-4af7-8b79-24294d7c47b3)

<h1>Task-3</h1>
 <h2> Create a new EC2 Instance </h2>
 
• Launch an instance by creating an windows EC2. Give a name for your 
instance.  

![image-2](https://github.com/user-attachments/assets/e90cf259-5430-4bbb-bb77-04db660ed67c)

• Choose an Amazon Linux as the operating system from the windows 
section. 

![image-3](https://github.com/user-attachments/assets/950f972a-35b6-469e-b338-39cdcd4f3dfb)


<h1>Task-4</h1>

•  Create a new key pair by giving any name for your key pair under RSA 
key type. 

• The key pair can be downloaded using .pem file format. 
The key pair is now created successfully.

![image-4](https://github.com/user-attachments/assets/941b1987-4fe8-44ac-9f8c-75cd5d71a77c)

<h1>Task-5</h1>

• In Network Settings, select an create security group that allow SSH on 
port 22(for connecting to the instance). Then allow HTTP on port 80(for 
accessing Nginx in a browser).

![image-5](https://github.com/user-attachments/assets/1305045d-0f06-49b0-9479-1d277acef1c0)

• Check for SSH and HTTP whether they are bound to their port 22 and 
80. 

<h1>Task-6</h1>

• click on launch instance option, it creates an new instance. 

![image-6](https://github.com/user-attachments/assets/976cca9f-5331-49eb-9343-1f496a9a37cc)

![image-7](https://github.com/user-attachments/assets/80acfcdf-05e3-4670-8936-630a9ee4d551)

<h1>Task-7</h1>

• Select your created instance and click on connect to make sure it 
connects to your instance. 

![image-8](https://github.com/user-attachments/assets/c0068cff-ae15-4165-951c-0bb327482e1c)

<h1>Task-8</h1>

• Open your terminal and connect to the instance using SSH. 

![image-9](https://github.com/user-attachments/assets/17998d6c-ba92-47bf-850b-6af0b7afff76)

<h1>Task-9</h1>

<h2> Docker Installation:</h2>

 • Give sudo yum update -y command to update the system. 

 ![image-10](https://github.com/user-attachments/assets/f7f8af40-0120-4358-b38a-9042ecdcb66b)

• Give sudo yum install docker -y command to Install docker. 

![image-11](https://github.com/user-attachments/assets/0581108e-8c87-4ccf-a76c-b7a56a8c3633)

• Give sudo service docker start command to start the docker service.

![image-12](https://github.com/user-attachments/assets/062d5d3b-c112-42b4-84b0-d858b80fb9b6)

• Enable the docker to start on boot using the command,  
sudo systemctl enable docker. 

![image-13](https://github.com/user-attachments/assets/2df69a0d-36da-4c69-8347-2f8b02a16ff1)

• Verify whether the Docker is installed using the command,  
docker --version. 

![image-14](https://github.com/user-attachments/assets/cb951434-0fab-4aed-8695-d2574077b5a3)

<h1>Task-10</h1>

<h2> Pull and Run the Nginx Container </h2> 

• Pull the Nginx image from the docker hub using the command,  
docker pull nginx. 

![image-15](https://github.com/user-attachments/assets/8bcc0c69-116f-4558-b2e5-48e5efc28fd5)

• Now run the nginx container using the command,  
docker run -d -p 80:80 –name nginx-container nginx. 

![image-16](https://github.com/user-attachments/assets/0cd19a69-f095-4c51-bd99-d73777eb4e28)

d : Runs the container in the background 

-p 80:80 : It maps port 80 of the EC2 instance to port 80 of the container.  

--name nginx-container : It names the container as nginx-container. 

• Verify whether the container is running by using the command,  
docker ps -a. 

![image-17](https://github.com/user-attachments/assets/23ff30e3-639e-43de-9d54-37e4697696e2)

• Thus the container should appear in the list of running containers. 

<h1>Task-11</h1>

• At last to access the nginx web server, copy paste the public ip 
address of your ec2 instance in any open browser and you must see the Nginx 
Welcome Page. 

![image-18](https://github.com/user-attachments/assets/3f16d252-57f7-44ca-92ee-12a5408de3ae)

<h1>Task-12</h1>
<h2>After launching a successfull website </h2>

https://github.com/user-attachments/assets/06f12411-d661-4be3-bf4c-1ae3dfa765ce



