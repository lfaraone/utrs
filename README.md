Getting started
===============

For an Ubuntu system:
    sudo apt-get install apache2 git libapache2-mod-php5
    sudo php5enmod json
    sudo service apache2 restart
    cp public_html/config.js.template public_html/config.js.php

Edit config.js.php with your settings. Most notably, you'll need to [create a ReCAPTCHA enlistment][1] and configure a database for UTRS to use. The database should be named `utrs_dev`; the provided database schema expects such a name.

The database schema is located in `mysql_schema.sql`. Apply it to the database via a tool like Workbench or `mysql -D utrs_dev < mysql_schema.sql`.

Finally, ensure the `public_html` directory is served by Apache. On Ubuntu systems, you can simply run `ln -s public_html /var/www/html/utrs`, then visit http://localhost/utrs.

[1]: https://www.google.com/recaptcha/admin


