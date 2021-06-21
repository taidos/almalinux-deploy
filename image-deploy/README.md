This will be an image of AlmaLinux for OpenVZ 7 or LXC VPS quest's 

For LXC you just need to download all the parts and decompress it!
For OpenVZ you need to install the EZ package made by blueonyx.it and then download the parts to your /vz/template/cache and unpack them

https://www.blueonyx.it/news/283/15/OpenVZ-7-AlmaLinux-OS-template-cache

Deploy on your node:

cd ~/
yum -y install p7zip.x86_64
git clone https://github.com/taidos/almalinux-deploy.git
rpm -Uvh ~/image-deploy/almalinux-8-x86_64-ez-1.0.0-1BX01.vl7.noarch.rpm
cd ~/almalinux-deploy/image-deploy/
7za -y x "almalinux-8-x86_64.tar.7z.*"
mv almalinux-8-x86_64.tar.gz /vz/template/cache
rf -rf ~/almalinux-deploy
