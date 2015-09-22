docker-cakephp
======================

Out-of-the-box CakePHP docker image


Usage
-----

You can edit the Dockerfile to add your own Github URL

To create the image `skywidesoft/cakephp`, execute the following command on the docker-cakephp folder:

	docker build -t skywidesoft/cakephp .

You can now push your new image to the registry:

	docker push skywidesoft/cakephp


Running your CakePHP docker image
-----------------------------------

Start your image:

	docker run -d -p 80:80 -p 3306:3306 skywidesoft/cakephp

	docker run -d -p 80:80 -p 3306:3306 -v /home/core/share:/app skywidesoft/cakephp

Test your deployment:

	curl http://localhost/

You can now start using your CakePHP container!

Connect to MySQL
----------------
mysql -h 127.0.0.1 -u admin -p
Password: Password1
