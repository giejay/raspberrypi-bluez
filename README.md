###### Introduction
This ansible project downloads, compiles and installs Bluez-5.41 including all pre-requisites on the Raspberry PI. To run, execute the following steps:

###### 1. login as 'pi' user

###### 2. Change to root user
```
sudo su -
```

###### 3. Install Ansible and Git
```
echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" >> /etc/apt/sources.list
apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
apt-get update
apt-get install -y ansible git
```

###### 4. Clone the Raspberry PI Bluez github project
```
git clone https://github.com/mkieboom/raspberrypi-bluez
cd raspberrypi-bluez
```

###### 5. Run the ansible scripts to install Bluez
```
ansible-playbook -i myhosts/raspberrypi_localhost raspberrypi-deployment.yml --connection=local
```

###### 6. Reboot the Raspberry PI
```
reboot
```
