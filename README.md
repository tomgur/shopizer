Shopizer 2.2.0 (for java 1.8 +)
-------------------

Java open source e-commerce software

To get the code:
-------------------
Clone the repository:
$ git clone git://github.com/tomgur/shopizer.git

To build the application:
-------------------	
From the command line with Maven installed:

	$ cd shopizer
	$ mvn clean install
	

Run the application from Tomcat 
-------------------
copy sm-shop/target/ROOT.war to tomcat or any other application server deployment dir

Increase heap space to 1024 m or at least 512 m

### Heap space configuration in Tomcat:


If you are using Tomcat, edit catalina.bat for windows users or catalina.sh for linux / Mac users

	in Windows
	set JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 
	
	in Linux / Mac
	export JAVA_OPTS="-Xms1024m -Xmx1024m -XX:MaxPermSize=256m" 
