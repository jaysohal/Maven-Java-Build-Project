# Maven Java Build Project

This is a simple java project that displays "Hello World" on CLI.

## Prerequisites
Maven - Install Apache Maven using ```sudo apt install maven``` and verify the installation with 
Java Developers Kit - Install JDK using 

## Initialize a Maven project
Create a new directory "maven-project" and initialize a new maven project using 

```mvn archetype: generate```

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/initialize.png)

Choose the default filter number.Ex: 1652 (it could be different for you). This creates a very simple Java project that displays "Hello World" in the CLI upon execution.

Next, enter the groupID, artifactID, version and package as shown in the screenshot. (You can change this to anything else that is sensible)

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/initialize1.png)

This will create a new project in your directory with the following structure. In this case, you already have the App.java file and you can go ahead and start packaging this into an executable file. 

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/initialize2.png)

## Maven Build Lifecycle

### STEP 1 Validate
Validate the project is correct and all the necessary information is available. 

```mvn validate```

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/validatecompile.png)


### STEP 2 Compile
Compile the source code of the project. Note: If you get an error, go into pom.xml file and update the dependecies to lates Maven version(ex: change it from 1.7 to 1.8)


```mvn compile```

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/validatecompile.png)

This will also create a new folder ```target``` in your directory. 

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/target.png)


### STEP 3 Test
Test the compiled source code using a suitable unit testing framework. It will execute whatever tests you have in the test folder of your project. These tests should not require the code to be package or deployed

```mvn test```

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/test.png)


### STEP 3 Package
Take the compiled code and package it in its distrubutable format, such as JAR or WAR. 

```mvn package```

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/package.png)

After this command you can see a ```.jar``` file created under the ```target``` folder. 

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/jarfile.png)

### STEP 4 Verify
Run any checks on result of integration tests to ensure quality criterias are met

```mvn verify```

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/verify.png)


### STEP 5 Install
Intall the package into local repository, for use as a dependecy in other projects locally

```mvn install```

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/install.png)

### STEP 6 Deploy
For this you will need the following: 
Name of your .JAR file. You can find it under your ```target``` folder. 
Name of your Java App: You can find it in your ```App.java``` file. You can get it by running the following command. Make sure to change "your_app_name" with your own custom app name. 

```cat src/main/java/com/your_app_name/demo/App.java```

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/appname.png)

Once you have these two, then navigate into the ```target``` folder and execute the following. Make sure to change "your_jar_file_name" and "your_app_name" to your own.

```java -cp your_jar_file_name your_app_name.App```

![alt text](https://github.com/jaysohal/Maven-Java-Project/blob/main/images/deploy.png)



This will execute your Java code and perform the desired action. 





 





