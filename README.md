# azuracast-docker-aws

sudo amazon-linux-extras install docker

sudo service docker start

sudo usermod -a -G docker ec2-user

sudo chkconfig docker on

sudo yum install git

sudo reboot

#Az újraindulás után:

sudo curl -fsSL https://github.com/docker/compose/releases/download/v2.4.1/docker-compose-linux-$(uname -m) -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

git clone https://github.com/gyozo-cloud/azuracast-docker-aws

cd /home/ec2-user/azuracast-docker-aws/azuracast

docker-compose up -d

#Az Azuracast szerver leállítása:

cd /home/ec2-user/azuracast-docker-aws/azuracast

docker-compose down

#Az Azuracast szerver indítása, az AWS instance indítás után:

cd /home/ec2-user/azuracast-docker-aws/azuracast

docker-compose up -d
