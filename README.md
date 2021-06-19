# docker-on-aws-ec2 using Amazon Linux AMI instance (Amazon Machine Image)
Configure docker on AWS EC2 instance

### For this I suppose a runnig AWS instance created. 
If not then please refer the section on this repo : https://github.com/avinashkumar-github/jenkins-on-aws-ec2#aws-ec2-instance---free-tier-specific

Can SSH into the Virtual machine or EC2 instance, and execute the following commands to configure Docker.
```
sudo yum update -y  //To update all binaries if outdated
sudo yum install docker -y  // To install docker binary
docker -v  //To check the version that installed
sudo service docker start // start the docker as a service

sudo usermod -a -G docker ec2-user  // Adding the ec2-user or any other user respective to the instance machine on to the docker group. To avoid using the "sudo" on below listed commands. Alternative can use below command by placing sudo at the front

docker images  // To list all the available images in docker
docker ps  //To list all the available container of image
docker info  //To get the information about the installed docker

```
