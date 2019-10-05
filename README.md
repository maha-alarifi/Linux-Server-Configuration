
# Linux Server Configuration
## Project of Udacity Fullstack Web Development Nanodegree

### IP Address : `3.123.1.136`

### URL


### Summary of Software Installed
- finger : `sudo apt-get install finger` (this application retrieve information about users)
- Apache : `sudo apt-get install apache2`
- PostgreSQL : `sudo apt-get install postgresql`
- mod_wsgi : `sudo apt-get install libapache2-mod-wsgi`
- python : `sudo apt-get install python-dev`
- git : `sudo apt-get install git`
- Flask : `pip install Flask`
- SQLALchemy : `sudo pip install sqlalchemy`
- sqlalchemy_utils : `sudo pip install sqlalchemy_utils`
- psycopg2 : `sudo pip install psycopg2`
- httplib2 : `sudo pip install httplib2`
- oauth2client : `sudo pip install oauth2client`
- pip : `sudo apt-get install python-pip`



### Summary of Configurations Made
- Create an instance in AWS Lightsail
- Change time zone to UTC `sudo dpkg-reconfigure tzdata`
- System reboot after all the setting is done


#### User Management
- Can you log into the server as the user grader using the submitted key?
  1. `sudo adduser grader`

- Is remote login of the root user disabled?
  1. `sudo nano /etc/ssh/sshd_config`
  2. delete _prohibit-password_  but instead *no*
  3. `sudo service ssh restart`

- Is the grader user given sudo access?
  1. `grader is added to /etc/sudoers.d/`

#### Security
- Is the firewall configured to only allow for SSH, HTTP, and NTP?
  1. `sudo ufw default deny incoming`
  2. `sudo ufw default allow outgoing`
  3. `sudo ufw enable`

- Are users required to authenticate using RSA keys?
  1. `ssh-keygen`
  2. passphrase : `toor`

- Are the applications up-to-date?
  1. `sudo apt-get update` (This command do not update the system but actually making sure that the softwares are aware of the available updates)
  2. `sudo apt-get upgrade` (This command actually updates the softwares)
  3. `sudo apt-get autoremove` (This command removes packages that are no longer required automatically)

- Is SSH hosted on non-default port?
  1. `sudo nano /etc/ssh/sshd_config`
  2. change 22 to 2200
  3. `sudo service ssh restart`

#### Application Functionality
- Is there a web server running on port 80?
- Has the database server been configured to properly serve data?
- Has the web server been configured to serve the Item Catalog application?

### list of third-party resources
