#Getlancer -Bidding

Getlancer-Bidding is an effective Freelancing script which helps the entrepreneur to run a successful freelancing website. It is written in AngularJS with REST API for high performance in mind. Top of above, we provide this comprehensive script in absolutely free of cost.

This is project is part of Agriya Open Source efforts. Getlancer-Bidding was originally a paid script and was selling around $ 10000. It is now released under dual license (OSL 3.0 & Commercial) for open source community benefits.

## Support

Agriya's Getlancer-Bidding is an open source project. Full commercial support (commercial license, customization, training, etc) are available through [Freelancer Clone Script Support](https://www.agriya.com/products/freelancer-clone)

Theming partner [CSSilize for design and HTML conversions](http://cssilize.com/)


Installation Steps
------------------
# Server Requirements

    ** PHP Version - PHP >= 5.6
        * Extensions
            GD Version - 2.x+
            PCRE Version - 7.x+
            cURL version - 7.x+
            json version - 1.x+
            OpenSSL
            PDO PHP Extension
            mbstring
        * php.ini settings
            max_execution_time - 180 (not mandatory)
            max_input_time - 6000 (not mandatory)
            memory_limit - 128M (at least 32M)
            safe_mode - off
            open_basedir - No Value
            display_error = On
            magic_quotes_gpc = Off
    ** postgres sql : 9.4
    ** ngnix server
        Nodejs
        Composer
        Bower
        Grunt
    Recommended Linux distributions: Centos / Ubuntu / RedHat
    
    ## Getting Started

### Prerequisites

#### For deployment

* PostgreSQL
* PHP >= 5.5.9 with OpenSSL, PDO, Mbstring and cURL extensions
* Nginx (preferred) or Apache

#### For building (build tools)

* Nodejs
* Composer
* Bower
* Grunt

### Setup

* PHP dependencies are handled through `composer` (Refer `/server/php/Slim/`)
* JavaScript dependencies are handled through `bower` (Refer `/client/`)
* Needs writable permission for `/tmp/` and `/media/` folders found within project path
* Build tasks are handled through `grunt`
* Database schema `/sql/oliker_with_empty_data.sql`

### Contributing

Our approach is similar to Magento. If anything is not clear, please [contact us](https://www.agriya.com/contact).

All Submissions you make to Oliker through GitHub are subject to the following terms and conditions:

* You grant Agriya a perpetual, worldwide, non-exclusive, no charge, royalty free, irrevocable license under your applicable copyrights and patents to reproduce, prepare derivative works of, display, publicly perform, sublicense and distribute any feedback, ideas, code, or other information ("Submission") you submit through GitHub.
* Your Submission is an original work of authorship and you are the owner or are legally entitled to grant the license stated above.


# Server Side

### Composer Updation

To Update the Composer, please run the below command in your Project Path.  

* Path - server/php/Slim

        composer install
    
* The above Updation doesn't work to you, need to install Composer, please refer this link **https://getcomposer.org/**  for "**How to install Composer**".

### Database Settings

	* Path - server/php/config.inc.php

    * define('R_DB_DRIVER', 'pgsql');
	* define('R_DB_HOST', 'localhost');
	* define('R_DB_NAME', 'DBNAME');
	* define('R_DB_USER', 'DBUSER');
	* define('R_DB_PASSWORD', 'DBPASSWORD');

### Create database for your project

* Import db from the script

 	sql/getlancer_with_sample_data.sql

# Front Side: 

### You need to install nodejs, bower, grunt.

Go to the path in command prompt. "/client/

* Run the below command, the bower used to download and installed all front-end development libraries.

        bower install

* The npm used to install the all dependencies in the local node_modules folder.

        npm install    

### Need write permission for following folders recursively
 
		/media
		/tmp
		/client/images
		/scripts(only main folder not recursive)				
		/server/php/Slim/shell
 
### Setting up cron
			
        ## Common
        	*/2 * * * * /##DOC_ROOT_PATH/##PROJECT_NAME/server/php/Slim/shell/main.sh 1» /##DOC_ROOT_PATH/##PROJECT_NAME/tmp/logs/shell.log 2» /##DOC_ROOT_PATH/##PROJECT_NAME/tmp/logs/shell.log

        ## Jobs Plugin
		    */2 * * * * /##DOC_ROOT_PATH/##PROJECT_NAME/server/php/Slim/shell/subscription.sh 1» /##DOC_ROOT_PATH/##PROJECT_NAME/tmp/logs/shell.log 2» /##DOC_ROOT_PATH/##PROJECT_NAME/tmp/logs/shell.log
		
		    */2 * * * * /##DOC_ROOT_PATH/##PROJECT_NAME/server/php/Slim/shell/job.sh 1» /var/www/html/tmp/logs/shell.log 2» /var/www/html/tmp/logs/job.log
     
     
     
     ### License

Copyright (c) 2014-2018 [Agriya](https://www.agriya.com/).

Dual License (OSL 3.0 & [Commercial License](https://www.agriya.com/contact))
