NOHRM
==========

NOHRM is a free and powerful new-age Human Resource Management System that can be easily configured to adapt to your organizational processes.



Installing NOHRM
=================



Table of Contents:

1. What server NOHRM works on?
2. Windows installation Guide 
3. Linux installation Guide 
4. MAC installation Guide 
5. Upgrading your application code with patches

	1. What server does NOHRM work on?
	=======================================
	NOHRM works only on Apache Server

	2. Windows Installation Guide 
	=============================
		AMP stack for Windows
		---------------------
		- The recommended AMP stack for Windows is XAMPP (Download the installer from basic package)
		- The system installer for XAMPP will guide you through the installation process

		Copying files 
		-------------
		- Move NOHRM zip file into the document root of Apache HTTP server.
		- If you used XAMPP for windows, document root is   <XAMPP installed location>\htdocs\
		- For example: C:\xampp\htdocs\

		Extracting 
		----------
		- Extract the NOHRM zip file in the document root of Apache HTTP server

		Web Installer  
		-------------
		- XAMPP users; the AMP stack for Windows needs to be started manually.
		- Using a JavaScript enabled browser go to http://<webhost>/nohrm/; Where <webhost> is localhost if it is installed in the machine you are
		currently working on, IP address if it is remotely hosted 
		
		Pre-requisites
		--------------
		The system requirements for installing NOHRM are described below. Make sure your system meets these requirements.

		a. PHP 5.3 or later
			You can download PHP 5.3 or later by visiting http://windows.php.net/download/

		b. PDO MySQL (for MySQL connection) 
			To install NOHRM on windows, you need to enable the PDO and PDO_MYSQL extensions in your php.ini file. You can add the following
			 lines in your php.ini file:

			1. extension=php_pdo.dll
			2. extension=php_pdo_mysql.dll
		
		c. Rewrite module (for working of MVC architecture)
			To activate the module, the following line in httpd.conf needs to be uncommented:

			1. LoadModule rewrite_module modules/mod_rewrite.so
			To see whether it is already active, try putting a .htaccess file into a web directory containing the line

			2. RewriteEngine on
			If this works without throwing a 500 internal server error, and the .htaccess file gets parsed, URL rewriting works.

			You also need to make sure that in your httpd.conf, AllowOverrides is enabled:

			3. AllowOverride all
			This is important as many httpd.conf ship by default with allowoverride none

		d. GD library (for images)
			You can add the following lines in your php.ini file:

			1. extension = php_gd2.dll
		
		e. Open SSL (For SSL and TSL Protocols)
			Download the installer for OpenSSL 1.0.1e from http://www.openssl.org/related/binaries.html

			If OpenSSL is already installed in your system, to enable this extension in your php.ini file, you can add the following line in your php.ini
			file:

			1. extension=php_openssl.dll

	3. Linux Installation Guide 
	===========================
		AMP stack for Linux
		-------------------
		- The recommended AMP stack for Linux is XAMPP Linux 1.6 (Download the complete stack and not the upgrades)
		- The system installer for XAMPP in the XAMPP site will guide you through the installation process
		- Start the stack manually every time you reboot.
		- Change the ownership of NOHRM files (Ex: /opt/xampp/htdocs/NOHRM/ $ chown -R nobody.nobody)

		Copying files 
		-------------
		- Move NOHRM zip file into the document root of Apache HTTP server.
		- If you used XAMPP for windows, document root is   <XAMPP installed location>\htdocs\
		- For example: C:\xampp\htdocs\

		Extracting 
		----------
		- Extract the NOHRM zip file in the document root of Apache HTTP server

		Web Installer  
		-------------
		- XAMPP users; the AMP stack for Linux needs to be started manually.
		- Using a JavaScript enabled browser go to http://<webhost>/nohrm/; Where <webhost> is localhost if it is installed in the machine you are 
		currently working on, IP address if it is remotely hosted 
		
		Pre-requisites
		--------------
		The system requirements for installing NOHRM are described below. Make sure your system meets these requirements.

		a. PHP 5.3 or later

		b. PDO MySQL (for MySQL connection) 
			To install NOHRM on Linux, you can compile php with --with-pdo-mysql in your php.ini, and add the following lines:

			1. extension=pdo.so
			2. extension=pdo_mysql.so
		
		c. Rewrite module (for working of MVC architecture)
			activate mod_rewrite in linux, open the terminal and add the below line:

			1. sudo a2enmod rewrite
			
			You also need to make sure that in your httpd.conf, AllowOverride is enabled:
			2. AllowOverride All
			
		d. GD library (for images)
			To install GD library in Linux, open the terminal and add the below lines:
			
			1. #apt-get install php5-gd
		
		e. Open SSL (For SSL and TSL Protocols)
			Download the OpenSSL 1.0.1c tarball archive from the OpenSSL web site at http://www.openssl.org/source/

	4. MAC Installation Guide
	=========================
		AMP stack for MAC
		-----------------
		- The recommended AMP stack for MAC is MAMP 
		- The system installer for XAMPP will guide you through the installation process
		- If MAMP is previously installed, the installer will rename the MAMP folder to MAMP_current_date.
		- An existing <htdocs> folder will be moved to your new /Applications/MAMP folder.
		- Your /Applications/MAMP_current_date folder can now be deleted. You can keep it if you wish to fall back to your original setup.

		Copying files 
		-------------
		- Move NOHRM zip file into the document root of Apache HTTP server.
		- If you used XAMPP for windows, document root is   <XAMPP installed location>\htdocs\
		- For example: C:\xampp\htdocs\

		Extracting 
		----------
		- Extract the NOHRM zip file in the document root of Apache HTTP server

		Web Installer  
		-------------
		- MAMP users; the AMP stack for MAC needs to be started manually.
		- Using a JavaScript enabled browser go to http://<webhost>/nohrm/; Where <webhost> is localhost if it is installed in the machine you are 
		currently working on, IP address if it is remotely hosted
		
		Pre-requisites
		--------------
		The system requirements for installing NOHRM are described below. Make sure your system meets these requirements.

		a. PHP 5.3 or later
			You can download PHP 5.3 or later by visiting http://php.net/downloads.php

		b. PDO MySQL (for MySQL connection) 
			To install NOHRM on MAC, you need to enable the PDO and PDO_MYSQL extensions in your php.ini file. You can add the following lines in 
			your php.ini file:

			1. extension=php_mysqli.so
			2. extension=php_pdo_mysql.so
		
		c. Rewrite module (for working of MVC architecture)
			To activate mod_rewrite module in MAC, add the below line to httpd.conf file

			1. LoadModule rewrite_module libexec/apache2/mod_rewrite.so
			2. LoadModule php5_module libexec/apache2/libphp5.so
			
			Also, make sure that AllowOverride is set to All within the <Directory "/Library/WebServer/Documents"> section.

		d. GD library (for images)
			You can add the following lines in your php.ini file:

			1. extension = gd.so
		
		e. Open SSL (For SSL and TSL Protocols)
			Download the installer for OpenSSL from http://www.openssl.org/source/

