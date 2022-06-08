## Create EC2 instance 
      Install Apache and Dependencies
      In the terminal, install the Apache 2 web server, libraries, PHP, and PHP MySQL:

      sudo apt install apache2 libapache2-mod-php php-mysql
      When prompted, press Y for yes and hit Enter.

      Go into the newly created /var/www directory:

      cd /var/www
      View the contents of the directory:

      ls
      Put wordpress into its own folder in the /var/www directory that we're currently in:

      sudo mv /wordpress .
      View the contents of the directory:

      ls
      Move into the wordpress directory:

      cd wordpress
      Move the Apache configuration file into /etc/apache2/sites-enabled/ to enable the WordPress website to work from /var/www/wordpress:

      sudo mv 000-default.conf /etc/apache2/sites-enabled/
      Restart the Apache 2 configuration:

      sudo apache2ctl restart
      Open the WordPress config PHP file for editing:

      sudo nano wp-config.php
      Return to the browser window or tab that has the RDS Databases open.

      Click the wordpress database.

      In the Connectivity & security tab, under Endpoint, copy the endpoint provided into your clipboard.

      Return to your terminal.

      Change the line define('DB_HOST', 'localhost'); to read:

      define('DB_HOST', '<INSERT ENDPOINT HERE>');


## Create RDS Database 
