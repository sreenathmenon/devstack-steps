# Devstack Installation Steps

apt-get update
apt-get upgrade -y
reboot
apt-get -y install git
useradd -d /opt/stack -m -s /bin/bash stack  >> directory creation also happen here
echo "stack ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
Edit /etc/sudoers file
su - stack
pwd
/opt/stack
git clone https://git.openstack.org/openstack-dev/devstack
chmod -R 770 devstack/
chown -R stack:stack devstack/
cd devstack/
Now create a basic configuration file. A sample file is present in this repository (sample-local.conf file).
Run the command ./stack.sh
This will start the installation process.
