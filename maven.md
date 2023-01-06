mvn --version			
Prints out the version of Maven you are running.

mvn clean				
Clears the target directory into which Maven normally builds your project.

mvn package				
Builds the project and packages the resulting JAR file into the target directory

mvn package -Dmaven.test.skip=true	
Builds the project and packages the resulting JAR file into the target directory 
- without running the unit tests during the build.

mvn clean package	
Clears the target directory and Builds the project and packages the 
resulting JAR file into the target directory.

mvn clean package -Dmaven.test.skip=true	
Clears the target directory and builds the project and packages the 
resulting JAR file into the target directory - without running the unit 
tests during the build.

mvn verify	
Runs all integration tests found in the project.

mvn clean verify	
Cleans the target directory, and runs all integration tests found 
in the project.

mvn install	
Builds the project described by your Maven POM file and installs the 
resulting artifact (JAR) into your local Maven repository

mvn install -Dmaven.test.skip=true	
Builds the project described by your Maven POM file without 
running unit tests, and installs the resulting artifact (JAR) into 
your local Maven repository

mvn clean install	
Clears the target directory and builds the project described 
by your Maven POM file and installs the resulting artifact (JAR) 
into your local Maven repository

mvn clean install -Dmaven.test.skip=true	
Clears the target directory and builds the project described 
by your Maven POM file without running unit tests, and installs 
the resulting artifact (JAR) into your local Maven repository

mvn dependency:tree	Prints out the dependency tree for your project 
- based on the dependencies configured in the pom.xml file.

mvn dependency:tree -Dverbose	Prints out the dependency 
tree for your project - based on the dependencies configured 
in the pom.xml file. Includes repeated, transitive dependencies.

mvn dependency:tree -Dincludes=com.fasterxml.jackson.core	
Prints out the dependencies from your project which depend on the 
com.fasterxml.jackson.core artifact.

mvn dependency:tree -Dverbose -Dincludes=com.fasterxml.jackson.core	
Prints out the dependencies from your project which depend on the 
com.fasterxml.jackson.core artifact. Includes repeated, transitive dependencies.

mvn dependency:build-classpath	
Prints out the classpath needed to run your project (application) 
based on the dependencies configured in the pom.xml file.








mvn clean ==> delete target folder
- mvn clean test ==> delete target folder
                     and run cucumber tests

- mvn clean verify ==> delete target folder, run cucumber test,
                       generate cucumber HTML report

- mvn clean verify -P Regression ==> delete target folder,
                                 run Regression profile in pom.xml.

- mvn verify -Dfile = RegressionRunner.java ==>
                     runs this specific runner class

- mvn install -DskipTests ==> It will skip all tests

- mvn -Dtest=login test ==> Running a Single Test Class:
                            It will run only login test class

- mvn verify -Dbrowser=firefox --> to run with firefox

- mvn verify -Dbrowser=chrome --> to run with chrome

- mvn verify -Dcucumber.options="--tags @smoke" 

-Denv="QA2" --> provide scenarios that you want to run.
No need to change CucumberRunner class. 
It overrides runner class configuration.