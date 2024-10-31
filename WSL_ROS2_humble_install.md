# WSL install ROS2 Humble install

##  시스템의 로케일이 UTF-8로 설정
~~~
 locale  
 #현재 locale setting 이 UTF-8 로 설정되어 있는지 확인

sudo apt update && sudo apt install locales 
#PACKAGE UPDATE , locale package install

sudo locale-gen en_US en_US.UTF-8  
#미국 표준 인코딩 설정, en_US.UTF-8로 locale 설정

sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8 
#시스템의 로케일 환경 변수를 업데이트해서 LC_ALL과 LANG을 en_US.UTF-8로 설정

export LANG=en_US.UTF-8 
# 현재 세션에 LANG 변수를 en_US.UTF-8로 설정

locale  
# en_US.UTF-8로 제대로 설정되었는지 확인

~~~
# Setup Sources
* Ubuntu Universe repository is enabled.
~~~
sudo apt install software-properties-common
sudo add-apt-repository universe
~~~
* Now add the ROS 2 GPG key with apt
~~~
sudo apt update && sudo apt install curl -y
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
~~~
* Then add the repository to your sources list.
~~~
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
~~~

# Install ROS 2 packages
* ubuntu upgrade and update
~~~
sudo apt update && sudo apt upgrade
~~~

* Desktop INSTALL : ROS , rvix, DEMOS , TUTORIAL
~~~
sudo apt install ros-humble-desktop
~~~
* Devlopment tools install 
~~~
sudo apt install ros-dev-tools
~~~

# install clcon
 ~~~
 sudo apt install python3-colcon-common-extensions
 ~~~
 
