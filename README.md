# ntbd_web
Robotic arm control and visualization web files for the ntbd project

This repository contains the web files for the ntbd robotic arm control.

# ntbd_ web requirements

Depend on the following ros packages:
- rosbrige_suite (see bellow)
- ntbd_core
- ntbd_msgs

Also depends on:
- ntbd_firmware
- httpd server, ex: nginx (see bellow)

Further ir requires an arm description ros package with the urdf, scripts and launch files required for ntbd, like the following:
- ebamk1_description
- ebamk2_description

# rosbrige install
sudo apt-get install ros-melodic-rosbridge-suite

# nginx install

sudo apt install nginx
sudo systemctl disable nginx.service

sudo service nginx status
sudo service nginx stop
sudo service nginx start

# ntdb_web install

cd /var/www/html/
git clone https://github.com/inaciose/ntbd_web

Copy the previous cloned <arm_description> package to the ntbd_web folder
We may have more than one arm description package in ntbd_web folder.

# ntdb_web usage

roslaunch <arm_description> ntdb_web.launch 

Point the browser to: http://localhost/ntdb_web
Use the sliders on bottom to set the desired position an execute

# related repositories

- https://github.com/inaciose/ntbd_base
- https://github.com/inaciose/ntbd_firmware
- https://github.com/inaciose/ebamk1_description
- https://github.com/inaciose/ebamk2_description

