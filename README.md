Tikal - Home Task - Tom Gur
-------------------

The Project is a Java open source e-commerce software forked from Github

*Tested with JDK1.8*

*Compilation with JDK1.10 failed miserably*


To get the code:
-------------------
Clone the repository:
$ git clone git://github.com/tomgur/shopizer.git

To build the application:
-------------------	
From the command line with Maven installed:

	$ cd shopizer
	$ mvn clean install
	
Docker Image - (only after mvn install)
------------
From the command line with Docker installed

    $ cd sm-shop
    $ docker build -t shopizer
    $ docker run -d -v /tmp:/tmp -p 8080:8080 shopizer
	
Run the application from Tomcat 
-------------------
copy sm-shop/target/ROOT.war to tomcat or any other application server deployment dir

If you are using Tomcat, edit catalina.bat for windows users or catalina.sh for linux / Mac users

	in Windows
	set JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 
	
	in Linux / Mac
	export JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 

Jenkins server
---------------
Jenkins is running in a Docker container in an EC2 instance

http://ec2-18-130-111-175.eu-west-2.compute.amazonaws.com:8080

Push to this github repo will trigger a webhook 
Calling the shopizer-pipeline job

Ansible
-------
Docker enabled hosts were configured with the install_docker playbook under ansible/playbooks



