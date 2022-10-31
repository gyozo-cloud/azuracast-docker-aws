# azuracast-docker-aws

sudo amazon-linux-extras install docker

sudo service docker start

sudo usermod -a -G docker ec2-user

sudo chkconfig docker on

sudo yum install git

sudo reboot

#Az újraindulás után:


git clone https://github.com/gyozo-cloud/azuracast-docker-aws

cd /home/ec2-user/azuracast-docker-aws/azuracast

sudo cp docker-compose /usr/local/bin

sudo chmod +x /usr/local/bin/docker-compose

docker-compose up -d

#Az Azuracast szerver leállítása:

cd /home/ec2-user/azuracast-docker-aws/azuracast

docker-compose down

#Az Azuracast szerver indítása, az AWS instance indítás után:

cd /home/ec2-user/azuracast-docker-aws/azuracast

docker-compose up -d
