---------------------------------------------------
Installing Application
---------------------------------------------------
1. Update OS
	$ sudo apt-get update

2. Install PIP (Python package repo)
	$ sudo apt-get install python-pip python-dev build-essential 
	$ sudo pip install --upgrade pip 
	$ sudo pip install --upgrade virtualenv

3. Clone the 'accessManager' repository
	$ cd /home/[desiredUserDir]/
	$ git clone https://github.com/malamaker/accessManager.git
	$ cd /home/[desiredUserDir]/accessManager/
	$ git checkout {dev/master}
	$ git pull

4. Setting the app to start on boot
	$ sudo cp /home/[desiredUserDir]/accessManager/accessManager /etc/init.d/
	$ sudo chmod 755 /etc/init.d/accessManager
	$ sudo update-rc.d accessManager defaults
	$ sudo shutdown -r now


---------------------------------------------------
Installing Updates
---------------------------------------------------
$ service accessManager stop
$ cd /home/[desiredUserDir]/accessManager/
$ git pull

