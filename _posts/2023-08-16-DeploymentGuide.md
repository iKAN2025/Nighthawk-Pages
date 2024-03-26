---
layout: base
title: Deployment Guide 
type: tangibles
courses: { compsci: {week: 12} }
comments: true
---
** Deployment Quiz/Guide**

First, I used Teacher's portfolio and used it as a template for deployment practice.
I had an idea for a port number, but I logged in AWS EC2 terminal to find out if someone used it already.
<img width="1356" alt="Screenshot 2024-03-23 at 3 50 14 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/f38b31d7-5364-4538-9f46-0fcb8148acec">
Then, I changed the port in the main.py, Dockerfile. and Dockercompose.yml file and checked to see if the port changed. I also commit these changes so the AWS EC2
 terminal can recognize the changes (when the git clone happens).
Docker.compose.yml
<img width="765" alt="Screenshot 2024-03-23 at 3 34 57 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/cc21e87e-2b2d-4580-b4ce-68a70a8168d6">
Dockerfile
<img width="502" alt="Screenshot 2024-03-23 at 3 44 31 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/13aa0382-05b1-4686-a09c-e553978252aa">
Main.py
<img width="444" alt="Screenshot 2024-03-21 at 10 36 17 AM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/00f1fb94-e850-4ad5-b5d6-ab857d6f992c">
Then,  I put docker compose build into the terminal. Since I got permission denied, I had to use sudo docker compose build and enter my password(admin). 
<img width="655" alt="Screenshot 2024-03-21 at 10 38 20 AM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/2dfa6960-e391-4c38-b649-ec9f0cf4c1de">
Here, I forgot to open my docker app.
<img width="695" alt="Screenshot 2024-03-21 at 10 47 12 AM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/964747fb-5e25-4e13-8aec-91795136cfa0">
Here, I forget to remove config.json (rm config.json)
<img width="727" alt="Screenshot 2024-03-21 at 10 48 18 AM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/aacbad8e-9338-4bb4-82d4-746731f5a05c">
Here,I run the container and check the link to see if it's working.
<img width="681" alt="Screenshot 2024-03-21 at 10 54 14 AM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/55711607-9331-49f5-a3c1-78fe02a1ec1e">
<img width="936" alt="Screenshot 2024-03-21 at 10 55 21 AM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/fd2d8c17-f6e4-4fd5-b7ed-48b124f1cea6">
<img width="1423" alt="Screenshot 2024-03-23 at 3 47 53 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/ac78eea0-72f3-4bf9-82c2-c0141612a2ae">
Now, I make sure to stop the container so I can start deploying.
<img width="343" alt="Screenshot 2024-03-23 at 3 52 59 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/ca706a88-51e9-4578-973d-208715f53e3d">
Then, I used this guide to start the commands in the terminal: [AWS Deployment Guide](https://nighthawkcoders.github.io/teacher//c7.0/c7.1/c7.2/2023/09/27/aws-deployment_IPYNB_2_.html#on-localhost-setup-docker-files-using-vscode)

Here are the first few commands:
<img width="838" alt="Screenshot 2024-03-23 at 3 55 53 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/1f4f38a8-0f2b-4f14-b2fa-7499d614a9a1">
Here is the container built/curl displaying html contents of home page. 
<img width="521" alt="Screenshot 2024-03-23 at 4 05 37 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/898e350c-32b2-4362-868d-434c6ab3faa5">

Then I moved on to route 53/created a record. 
<img width="1114" alt="Screenshot 2024-03-23 at 4 10 41 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/639a7143-06d9-4b8f-aea1-7ec1c40f0aca">

There was an error with the nginx config file: 
nginx: [emerg] could not build server_names_hash, you should increase server_names_hash_bucket_size: 64
nginx: configuration file /etc/nginx/nginx.conf test failed

I opened the file and increased the bucket size.

<img width="900" alt="Screenshot 2024-03-23 at 5 09 13 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/e944d8ce-380c-4453-84c9-ec2dd3c15105">

Then I was able to deploy following the instructions on the [AWS Deployment Guide](https://nighthawkcoders.github.io/teacher//c7.0/c7.1/c7.2/2023/09/27/aws-deployment_IPYNB_2_.html#on-localhost-setup-docker-files-using-vscode)

<img width="1430" alt="Screenshot 2024-03-23 at 5 12 08 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/2098befd-370a-4494-b6c0-0f87b0e3599d">


Then, after Cerbot Config, using [AWS Deployment Guide](https://nighthawkcoders.github.io/teacher//c7.0/c7.1/c7.2/2023/09/27/aws-deployment_IPYNB_2_.html#on-localhost-setup-docker-files-using-vscode)
W/interference
<img width="1433" alt="Screenshot 2024-03-23 at 5 17 02 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/de45b246-9857-4b4a-a570-26dc638c80c1">
Secure
<img width="754" alt="Screenshot 2024-03-23 at 5 25 11 PM" src="https://github.com/iKAN2025/DeploymentPractice1/assets/142475176/17f02912-c609-404f-9e5f-88a1dcdbb8eb">









