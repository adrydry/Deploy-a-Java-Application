We will use AWS console for this project

**Step 1 - Create our Security group. Make sure to open the open 80**

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/50e0cbf9-ca75-4934-a15b-012e24d4550d)

**Step 2 - Launch our EC2 instance**

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/eeaaf7c4-9c95-484d-8dc0-30a5f1f2f238)

**Step 3 - Connect to our EC2 server using mobaxterm**

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/e948f5d7-e24b-4e25-b789-b7fe0f40b969)

**Step 4 - Install java and Maven on this server**

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/6c922cf4-b301-4de6-86c8-cb5ae6d2bb22)

**Step 5 - clone the repository where the code is located**

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/daadbb8b-747b-40f6-8d05-ffb5716ea78d)

**Step 6 - Run mvn validate**

This will validate the pom.xml 

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/36e0cf6f-baa1-4a83-94ef-3faf972d6517)

**Step 7 - Run mvn compile**   

This will validate first the src and next check if there is an error in the syntax of the src

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/cd100342-569b-43d4-aed5-da7d60584c03)

After the mvn compile, a new folder **target** is created.

**Step 8 - Run mvn test**      

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/7fadec0b-684c-4fd8-8145-a2c6e355abd2)

**Step 9 - Run mvn package** 

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/07538c83-5c30-4845-92b6-529cb3637614)

Our Jar file is created and located in the target folder. This is our application. If executed, the application will begin to run

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/eb53908f-0d7a-40ca-a595-e0a57cff7ef1)

**Step 10 - Run mvn install**   
We noticed a failure because we ran the mvn install inside the target folder which doesn't have the pom.xml. So we need to go to the previous step with cd .. to run this command

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/982a991e-775f-4dc5-bb89-c2a4f44b1563)

This command install the jar file in the .m2 directory

**Step 11 - Run mvn deploy**

**Step 12 - Execute the java project

- Identify the location of the jar file: inside the target folder;

- Execute the jar file: **java -jar target/spring-boot-web.jar**

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/40c6d71a-3463-4ce8-8b32-d1fd7ff7cc0a)

Our application is executed

**Step 13 - Access the application**

The application is running on Tomcat, port 8080
IP: 8080 to access the application

![1](https://github.com/adrydry/Deploy-a-Java-Application/assets/102819001/51741b00-2172-4aba-b36c-b1cfa12728ac)

