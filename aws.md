### CloudFront, S3 (HTTPS with my own domain)

* SNI Issue - https://timnash.co.uk/building-cdn-ssl-cloudfront-certificates/
* Cetificate on in US-E region
* Redirect Option


### install script (docker, docker compose, code-deploy agent) 

* code deploy agent 

```
sudo yum update
sudo yum install ruby
sudo yum install wget
cd /home/ec2-user
wget https://aws-codedeploy-us-west-2.s3.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto
sudo service codedeploy-agent status
rm install
```


* docker

```
sudo yum update -y
sudo yum install -y docker
sudo service docker start
sudo usermod -a -G docker ec2-user
docker info
```

* docker compose

```
sudo -i
curl -L https://github.com/docker/compose/releases/download/1.16.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose

docker-compose --version

```





### reference 
* install code deploy agent : http://docs.aws.amazon.com/codedeploy/latest/userguide/codedeploy-agent-operations-install-linux.html
* install docker : http://docs.aws.amazon.com/ko_kr/AmazonECS/latest/developerguide/docker-basics.html
* install docker compose : https://docs.docker.com/compose/install/#install-compose
* to run docker-compose as root : https://stackoverflow.com/questions/42920840/how-to-run-docker-compose-as-root-user-docker-cloud/46189988#46189988
