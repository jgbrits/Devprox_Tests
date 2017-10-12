# Devprox_Tests
Proficiency tests done for Devprox

This solution was created to fullfil the requirements for the prociency tests set by Devprox. This solution is a Web based application making use of HTML, CSS, JavaScript, PHP and MySQL.



To deploy this solution, you need to set up a development server on your local machine that will run the PHP server side code, and connect to a MySQL database.


Download the XAMPP PHP development environment from this link: https://www.apachefriends.org/index.html

For Windows, install XAMPP using the .exe file. (For other OS's please see their documentation).

It will install a xampp folder onto you C: drive. Navigate to this folder. Find the htdocs folder within the xampp folder.

Download the two solution folders from Github: Devprox_Test1 and Devprox_Test2. Copy and paste these two folders into the htdocs folder. XAMPP serves the Webpages from the htdocs folder.

Navigate to xampp/php/php.ini and make the following changes to this file to ensure that large files (e.g. 1 milllion records) will be processed and uploaded to the server without the operation timing out or running out of memory.

In your "php.ini" file:

1. search for the file_uploads directive, and set it to On

2. search for the upload_max_filesize directive, increase it to 500M

3. search for the post_max_size directive, increase it to 500M

4. search for the memory_limit directive, increase it to 1280M

5. search for the max_input_time directive, increase it to 1800

Save and close php.ini

Find the xampp-control.exe application inside the xampp folder. Open it. When the application starts, click on the start buttons next to Apache and MySQL. When it started, it will turn green, If it does not, it could mean that another application/s are using the default ports for either the Apache Webserver or the MySQL database. In that case, either free up those ports on your machine, or change the default ports using the config buttons.

Once both Apache and MySQL are started, you are ready to serve websites from your local server.

For test 1, open this link: http://localhost/Devprox_test1/index.php
For test 2, open this link: http://localhost/Devprox_test2/index.php

To check whether records were inserted into the database as per the test requirements, open this link in your browser: http://localhost/phpmyadmin/

When the application for test 1 was run and the form submitted, the database "dbdevproxtest1" with table "person" should have been created. View the records inside by clicking on the table name.

When the application for test 2 was run and the CSV file uploaded, the database "dbdevproxtest2" with table "csv_import" should have been created. View the records inside by clicking on the table name.







