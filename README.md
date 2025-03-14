# Jenkins-Hands-On

This Jenkins-Hands-on Projects automates deployment of a java package using :

![GitHub Badge](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=fff&style=flat) - Source Code management Tool

![Sonatype Badge](https://img.shields.io/badge/Sonatype-1B1C30?logo=sonatype&logoColor=fff&style=flat) Nexus - Artifactory Management Tool

![Apache Maven Badge](https://img.shields.io/badge/Apache%20Maven-C71A36?logo=apachemaven&logoColor=fff&style=flat) - Build Tool

![Apache Tomcat Badge](https://img.shields.io/badge/Apache%20Tomcat-F8DC75?logo=apachetomcat&logoColor=000&style=flat) - Server 

![Jenkins Badge](https://img.shields.io/badge/Jenkins-D24939?logo=jenkins&logoColor=fff&style=flat) - CI/CD Pipeline
 
1. Jenkins Master is created on a Amazon Workspace Ubuntu system @ port 8080

2. Install Nexus, Nexus will use port 8081 of the Amazon Workspace Ubuntu system
    - Create a new Maven2 Hosted repository in the Nexus and name it as 'apprepo'
   
   Screenshot:

   ![image](https://github.com/AmalSunny992/Jenkins-Hands-On/assets/169422802/5f0bffc0-7d5d-4fed-bf97-452bd72ca8b6)


3. Install Github, Maven and Nexus plugins in Jenkins

4. A pipeline project with name "javaapp" is created in the Jenkins

    Screenshot :

   ![image](https://github.com/AmalSunny992/Jenkins-Hands-On/assets/169422802/e35ce855-5e3e-4e4f-96e2-5284ce004692)

5. A Pipeline script is written as different steps as follows
    
    1. Stage : Checkout Code : This stage will get the source code from Github
    2. Stage : Maven Build Tool : This Stage will download and install Maven Build Tool
    3. Stage : Compile App : This stage will Compile the Source code using Maven
    4. Stage : Test App : This stage will Test the Source code using Maven
    5. Stage : Package App : This stage will Package the Source code using Maven and create a .war file
    6. Stage : Upload Artifact :  : This stage will Upload addressbook.war file to Nexus artifactory
    7. Stage : Tomcat Prerequisite installation :  : This stage will Install java for Tomcat
    8. Stage : Tomcat Server Installation : This stage will Install Tomcat Server on port 8082
    9. Stage : Deploy App to Server : This stage will Deploy the code to Tomcat Server

  View Pipeline script [here](./jenkins)

 6. Run the Script by clicking build now in Jenkins.

    ### ScreenShots of Jenkins: 
    ![image](https://github.com/AmalSunny992/Jenkins-Hands-On/assets/169422802/4687990e-cc79-4faa-a7b6-c233786ee479)
    ![image](https://github.com/AmalSunny992/Jenkins-Hands-On/assets/169422802/a1e3f586-8e72-4b66-8814-0d5f5618b1bc)
    ![image](https://github.com/AmalSunny992/Jenkins-Hands-On/assets/169422802/1c37be50-e5a8-4c13-a721-c465aec8060d)
    ![image](https://github.com/AmalSunny992/Jenkins-Hands-On/assets/169422802/e8130968-dab1-4f95-ba52-200704dbf2f3)


    ### Screenshots of Nexus:
    ![image](https://github.com/AmalSunny992/Jenkins-Hands-On/assets/169422802/b5409de1-995d-47af-9fd0-19518dddfe6b)

    ### Screenshots of App running on Tomcat Server:
    ![image](https://github.com/AmalSunny992/Jenkins-Hands-On/assets/169422802/d5ae9f52-65aa-4e92-b07a-6aafef67f19c)
    ![image](https://github.com/AmalSunny992/Jenkins-Hands-On/assets/169422802/0cfd256b-d232-4a67-8a8a-2c7375d7c0c3)



    
    
   
