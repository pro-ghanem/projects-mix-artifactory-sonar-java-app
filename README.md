# Project-B

## Jenkins - Tomcat  whith 2 ways 

1. mount a common folder between containers "jenkins-tomcat-1"

2. after deployment copy the generated way to a common mounted folder "jenkins-tomcat"

Please create the folders and give them the appropriate permission

## jenkins artifactory integration 

- please check Build Environment

 * Resolve artifacts 
 * send artifacts to artifactory 
 notes : 
 - the Maven Goal in this case is install Not package  because install means "deploy":either deploy yor artifact on the artifactory or maven local-artifactory
 - sonarqube in "Pre-Step" phase to test code quality (Quality Asurance) (QA) & it's configrations:
sonar.host.url=http://sonarqube:9000
sonar.projectKey=java-app1
sonar.sources=./src
sonar.language=java
- artifactory configured twice :
  1- at build Phase : to Resolve artifacts from Artifactory (store building-binaries in the artifactory to increase the latency at building)
  2- at Post-Build Action : to deploy the artifact in the artifatory 
