# linux-server

The IP address to access the server is at: 35.164.145.44. The SSH port is 2200.

To access the URL of the hosted application please go to: http://35.164.145.44/

The list below shows the software which was installed on the machine:

	1. finger
	2. apache2
	3. python-pip python-dev build-essential
	4. sqlalchemy
	5. python-sqlalchemy
	6. python-psycopg2
	7. google-api-python-client 
	4. pip apps
		a. WTForms
		b. flask

Configuration changes:
	1. Created a new user named grader.
	2. Gave the grader the permission to sudo.
	3. Updated all currently installed packages.
	4. Changed the SSH port from 22 to 2200.
	5. Configured the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
	6. Configured the local timezone to UTC.
	7. Cloned item catalog git repository to ~/catalog/item_catalog.
	8. Created symbolic link to /var/www/html/catalog/. 
	9. Created /var/www/html/catalog/catalog.wsgi.
	10. Updated /etc/apache2/sites-enabled/000-default.conf to point to catalog.wsgi.
	11. Created postgres user catalog and gave limited permissions.
	12. Added database to be used for the item catalog application.
	13. Updated some hardcoded paths in ~/catalog/item_catalog to work with apache and wsgi.
	14. Change permissions of ~/catalog/item_catalog/static/images to give ownership to: www-data:www-data so apache can download images.

Third party sites I used to help me:
	1. Udacity
	2. Stackoverflow
	3. Google Searches
		a. http://www.datasciencebytes.com/bytes/2015/02/24/running-a-flask-app-on-aws-ec2/
		b. http://killtheyak.com/use-postgresql-with-django-flask/

