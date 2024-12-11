¬

 
NOTICES 
This information was developed for products and services offered in the U.S. IBM may not offer the products, services, or functionality described herein in other countries. Please consult your local IBM representative for information on products and services currently available in your region. Any reference to an IBM product, program, or service is not intended to state or imply that only that IBM product, program, or service may be used. Any functionally equivalent product, program or service that does not infringe any of IBM's intellectual property rights may be used instead. However, it is your responsibility to evaluate and verify the operation of any non-IBM product, program, or service.
IBM may have patents or patent applications pending that cover the subject matter described herein. Providing you with this document does not grant you any license to these patents. You may send your written license requests to: IBM IBM Corporation Licensing Director North Castle Drive, MD-NC119 Armonk, NY 10504-1785 United States of America
The following paragraph does not apply to the United Kingdom or any other country where such provisions are inconsistent with local law: INTERNATIONAL BUSINESS MACHINES CORPORATION PROVIDES THIS PUBLICATION "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF NON-INFRINGEMENT, MERCHANTABILITY, OR FITNESS FOR A PARTICULAR PURPOSE. Some states do not allow the disclaimer of express or implied warranties in certain transactions, so this statement may not apply to you.
This information may include technical inaccuracies or typographical errors. Changes are periodically made to the information contained herein; These changes will be incorporated into new editions of the publication. IBM may make improvements and/or changes to the products and/or programs described in this publication at any time without notice.
Any reference in this information to non-IBM sites is provided solely as a convenience and does not in any way serve as an endorsement of those sites. The materials on these sites are not part of the materials in this IBM product and your use of those sites is at your own risk.
IBM may use or distribute any information you provide in any way it deems appropriate, without incurring any obligation to you.
Information about non-IBM products has been obtained from the suppliers of those products, their published advertisements, or other publicly available sources. IBM has not tested these products and cannot confirm the accuracy of performance, compatibility or any other claims related to non-IBM products. Questions about the capabilities of non-IBM products should be directed to the vendors of those products.
This information contains examples of data and reports used in day-to-day business operations. To illustrate them as fully as possible, examples include the names of people, companies, brands, and products. All of these names are fictitious, and any resemblance to the names and addresses used by a real company is purely coincidental.
IBM TRADEMARKS, IBM logo and ibm.com are registered or are trademarks of International Business Machines Corp., registered in many jurisdictions around the world. Other product and service names may be trademarks of IBM or other companies. An up-to-date list of IBM trademarks is available on the web under "Copyright and Trademark Information" in www.ibm.com/legal/copytrade.shtml.
Adobe, the Adobe logo, PostScript, and the PostScript logo are registered or trademarks of Adobe Systems Incorporated in the United States and/or other countries. Cell Broadband Engine is a registered trademark of Sony Computer Entertainment, Inc. in the United States, other countries, or both, and is used under license therein. Intel, the Intel logo, Intel Inside, the Intel Inside logo, Intel Centrino, the Intel Centrino logo, Celeron, Intel Xeon, Intel SpeedStep, Itanium, and Pentium are registered trademarks or trademarks of Intel Corporation or its subsidiaries in the United States and other países.IT Infrastructure Library is a registered trademark of AXELOS Limited.ITIL is a registered trademark of AXELOS Limited.Java and all Java-based marks and logos are registered trademarks or trademarks of Oracle and/or its affiliates. Linear Tape-Open, LTO, the LTO logo, Ultrium, and the Ultrium logo are registered trademarks of HP, IBM Corp., and Quantum in the U.S. and other countries. Linux is a registered trademark of Linus Torvalds in the United States, other countries, or both. Microsoft, Windows, Windows NT, and the Windows logo are registered trademarks of Microsoft Corporation in the United States, other countries, or both. UNIX is a registered trademark of The Open Group in the United States and other countries. © Copyright International Business Machines Corporation 2020. This document may not be reproduced, in whole or in part, without the prior written permission of IBM. U.S. Government User Restricted Rights: Use, duplication, or disclosure restricted by GSA's ADP Program agreement with IBM Corp.




Index 

1 Introduction	4
Watsonx Orchestration Lab	4
2 Requirements for the laboratory	5
3 Case Introduction	6
3.1 Customer Scenario	6
3.2 Proposed solution.	6
3.3 Macro Fluxogram	7
4 Exercise: IBM RPA	8
4.1 Introduction of IBM RPA activities.	8
4.2 Creating a Credential	8
4.3 Edit your computer	9
4.4 Creating a Machine Group	10
4.5 Configure Private Key	11
4.6 Create Project	12
4.7 Add a robot to your project	14
4.8 Exercise: Download OpenAPI	17
4.9 Introduction to OpenAPI	17
4.10 Descargar da OpenAPI	17
4.11 Exercise: watsonx Orchestrate, how to publish a Skill.	17
4.12 Introduction	17
4.13 Criar Skill no watsonx Orchestrate.	17
4.14 Exercise: Exporting a Skill	22
4.15 Introduction	22
4.16 Exporting these skills	22
4.17 Exercise: Create a new AI Builder Wizard/Wizard	23
4.18 Introduction Ai Assistant Builder	23
4.19 Creating a New Wizard	23
4.20 Exercise: Creating the Conversation Flow Variables	33
4.21 Introduction	33
4.22 Exercise Statement - Creating Variables	34
4.23 Exercise: Creating the Conversational Flow	36
4.24 Introduction	36
4.25 Exercise: Final test	49
4.26 Introduction	49
4.27 Exercise Instruction	49
4.28 Exercise: Implementing AI Assistant and Builder	50
4.29 Introduction	50
4.30 Exercise Instruction	50


 
1 Introduction
Watsonx Orchestration Lab

IBM watsonx Orchestrate is an AI and generative automation solution that powers your business by automating tasks, streamlining complex processes, and ultimately saving time and effort for you and your team.  IBM watsonx Orchestrate offers:
•	Pre-built apps, skills, and wizards: The skills catalog contains thousands of predefined skills to help you perform a wide variety of tasks.
•	AI Assistant Builder: Quickly and easily create and deploy your purpose-built AI assistant with helpful conversations that help end users get the job done.
•	Skill Studio: Create your own custom skills and workflows without any coding experience.  More information here.


Lab Run Time: 3 hours
2 Requirements for the laboratory

1.	Have the webApptechJam app in the C:/Tech Jam 2024/ directory
 
Note: these files were sent by email to the participants of the laboratory, if you have not received them you can download them through the Official Git 

 https://github.com/AldoJustiniano-01/Tech-Jam-2024

Note: The script that is already published to your tenant accesses this directory and runs the index.html web file  in the path C:/Tech Jam 2024/webAppTechJam

2.	Access to LA Tech sales tenant, tenant must have been granted access, otherwise ask lab administrators.
 
3.	Acesso as URLS https://us1app.rpa.ibm.com/ e https://dl.watson-orchestrate.ibm.com




3 Case Introduction 
3.1 Customer Scenario


With the significant growth in the volume of operations in the insurance business unit, Focus Corps Bank faces challenges related to high demand and associated operating costs. Given the small team and time required to acquire new resources, the organization identified the need for an innovative solution to streamline the customer service process when it comes to insurance quotes. In response to this need, the Automations team was in charge of developing a technological solution capable of automating the online quote service through the insurer's portal. The main objective is to reduce the pressure on Customer Service (SAC) by ensuring that customers can access quotes quickly and autonomously, without the need for immediate human intervention.
The implementation of this solution will bring tangible benefits, such as the reduction of operating costs, the improvement of service efficiency and the freeing up of resources for higher value-added activities. In addition, automation will provide a faster and more convenient experience for customers, promoting greater satisfaction and retention. This initiative represents an important step towards the modernization of Focus Corps Bank's internal processes, reinforcing its commitment to deliver innovative and efficient solutions in the insurance sector.

3.2 Proposed solution.
To achieve these results, the automation team integrated watsonx Orchestrate into the operation, allowing them to exploit the full potential of this technology. The process was structured with the following elements:
•	watsonx Orchestrate: The business team developed a custom skill in Watson Orchestrate, capable of seamlessly integrating with IBM RPA. This integration made it possible to automate quotes in the insurance company's portal, eliminating manual steps and streamlining the process.
•	AI Assistant Builder: With this tool, the business team developed an intuitive flowchart that facilitates direct interaction with users on the insurer's main portal. The information collected during this conversation is automatically sent to watsonx Orchestrate, ensuring that all relevant data is processed accurately.
•	IBM RPA: This system captures the parameters generated in the conversation with the customer and, in an automated way, performs the query in the insurer's internal systems. At the end of the process, IBM RPA generates an email with the quote information and sends it directly to the requester, providing a faster and more efficient experience.




3.3 Macro Fluxogram
 

 
4 Exercise: IBM RPA
4.1 Introduction to IBM RPA activities.

In this lab, the InsuranceAuto.wal script, developed specifically to automate the insurance quoting process, is published to the control center and will be triggered directly by watsonX Orchestrate. For the integration between solutions to be effective, it is necessary to follow some important steps:
Create a project in IBM RPA Control Center: The first step is to set up a new project within Control Center to ensure that IBM RPA has the resources it needs to run the script efficiently.
Extract the OpenAPI file: After configuring the project, the next step is to extract the OpenAPI file, essential to define the communication interface between the systems and ensure the correct execution of the automated processes.

4.2 Create a credential
1.	Access the side menu and click on  "Credentials": Locate the menu on the left side of the screen and select the "Credentials" option to proceed with the setup.

 



2.	Click on the "Create credential"  button  to begin the process of creating a new credential.

 


3.	Enter a name for the credential: In the field provided, enter a descriptive name that makes it easy to identify the new credential.
 


4.	Enter the name of the Windows unlock user: In the appropriate field, enter the name of the user that will be used to unlock the computer on the Windows operating system.

 

5.	Enter the user's password: In the field provided, enter the password corresponding to the Windows unlock username
 

6.	Click Create

 

4.3 Edit your computer
7.	Go to the side menu and click "Computers": In the menu on the left of the screen.
 

8.	Click Computers.
 

1.	Find and locate your computer's name in the table: Use the available search field to make it easier to find your computer. Once you find them in the list, click on the three dots next to their name to access the options.

 

2.	Click Edit 
 
3.	Select Credential
 

4.	Click Save
 


4.4 Creating a Machine Group
5.	Click "Computers" in the left-side menu
 

6.	Click on Computer groups 
 

7.	Haga clic en Create computers group.
 





8.	Enter the name of the group: In the field provided, enter the name of the group. In this example, the name "TechJam" was used. 


9.	Select the computer: Choose, from the list, the computer where the script that manipulates the insurance company's system will be executed. Be sure to select the correct machine to ensure that the process is activated in the right environment. 

 


10.	Click Create

 


4.5 Configure Private Key

Configuring public and private keys  is a crucial process for data security in various applications, especially in asymmetric cryptography. This method uses two different keys to secure communication and ensure the authenticity of the data.

11.	Click on "Tenants" in the left side menu.
 

12.	Click on "Credentials".

 






13.	Verify the path of the private key: Confirm the path where the private key should be stored and create the corresponding directory in your environment, as shown in the image below.
 
 
4.6 Create project
14.	Click on "Projects" in the menu on the left side.

 
15.	Click on "Create project".
 


16.	Create Project Screen
Fill in the "Name" field: Since you are using the same Control Center with several users, it is important to avoid duplication in the creation of projects. To ensure exclusivity, please enter your name before the project name. For example, if your name is Marco, name the project " MarcoInsuranceAuto".

17.	Under Shared Access (optional), select "Everyone."
18.	Enter a Description for the project.
19.	Click Create.

 



20.	Success Message
Success message: Once the project is created, a success message will be displayed confirming that the process has been completed successfully.
 







4.7 Add a robot to your project
21.	Under "Manage Projects", locate your project: Find the project you created, which should contain the format "YourWebSafeName", and click on it to open it.
 
22.	Click "Create bot".
 


23.	Give the project a name, since we are using the same tenant, to avoid duplications, each user must customize the name of the project. Specify a name that begins with your own name. Example: "MarcoInsuranceAuto".


 

24.	Provide a description.

 
25.	Click Next
 


26.	Select the script. 
 

27.	Select the latest version.
 

Note: Always opt for the latest version. New versions may be released according to the development needs of this laboratory.


28.	Select the computer group.

 






29.	Click Next.
 


30.	The Summary screen appears, and then click "Create".
 

31.	A message will appear
  
4.8 Exercise: Download OpenAPI
4.9 Introduction to OpenAPI
An OpenAPI file is a document that describes the structure of an API, including its paths, methods, parameters, and responses, in a standardized format, usually using JSON or YAML. It allows developers and tools to easily understand and interact with the API, making it easy to document, test, and integrate.
Integration with Watsonx Orchestrate is done through an API, where several communication parameters are defined in this file.
Nota: https://www.ibm.com/docs/en/rpa/23.0?topic=projects-downloading-openapi-document
4.10 Descargar da OpenAPI
32.	Click Download "Download openAPI" and save the file to your directory. 
 
4.11 Exercise: watsonx Orchestrate, how to publish a Skill.
4.12 Introduction
A "Skill" in WatsonX Orchestrate is an automated capability or action that WatsonX can perform on behalf of the user. Skills allow WatsonX Orchestrate to integrate and interact with different applications, tools, or systems, performing specific tasks such as scheduling meetings, sending emails, obtaining data, or processing information in real time.
These skills are powered by APIs or predefined workflows and are built to automate repetitive processes and increase efficiency. The user can orchestrate multiple skills into a larger workflow to meet their operational needs in a smarter, more automated way.

4.13 Criar Skill no watsonx Orchestrate.

33.	Acesse a URL https://dl.watson-orchestrate.ibm.com/
34.	Enter User.
35.	Enter the password.
36.	Click Sign In.

 
37.	Click on the burger
 



Debs070513$

38.	Click Skill Studio

 


39.	Clique em Create Skill
 
40.	Click Import API
 
41.	Select the From a file option

 
42.	Drag the file or select it in the upload area

 
In this step, you will drag the . YML, which is the open API that you downloaded from IBM RPA control center projects. It will have your name and the name of the project you created.
 

43.	A checkmark should be displayed when uploading the file.
 
44.	Click Next

 

45.	Select Skill 
 

46.	Click Add
 .
47.	A success message will be displayed, you can manually close this message.
 
48.	The skill will be ready for publication

 

49.	Click on the three dots of your Skill and click on Enchance this skill
 
50.	Click Publish
 
Note: On this screen we can configure all user interaction in the handling within the watsonx orchestration chat, but for this lab we will create user interaction through the AI Build wizard.

51.	A display message will be posted. You can manually close this message.
 



4.14 Exercise: Exporting a Skill
4.15 Introduction
In this lab, we'll integrate watsonx Orchestrate with AI Assistant Builder. To do this, you'll need to export a skill .json file. The following are the steps to perform this procedure:
4.16 Export these skills
52.	To locate the skill list, you need to locate and click on the three dots of the skill. 
53.	Clique em export this skill. 

54.	Click Export this skill and save it to your directory.
 
4.17 Exercise: Create a new AI Builder Wizard/Wizard
4.18 Introduction to Ai Assistant Builder
In this exercise, we'll start creating a conversation flow in AI Assistant Builder. To do this, it is essential that each user creates their own dashboard, especially since we are sharing the same environment in this lab. In this way, we guarantee a better use of the available resources. In addition to the dashboard, we'll also create a new integration using a skill.json file. Next, we'll develop a conversation flow that will collect all the logs that will be sent via API to watsonx Orchestrate, which in turn will trigger the insuranceAuto.wal script on IBM RPA.

4.19 Creating a New Attendee
55.	From the main menu on the left side, go to Ai assistante builder
 

When the AI Assistant Builder is accessed for the first time, the assistant will need to be customized. If there are already other previously created wizards, steps 58 through 61 will not be displayed. In that case, continue from item 62

56.		Create your first attendee

 
57.	Customize your wizard and click Next

 


58.	Customize your attendee and click Next

 

59.	Click Create 

 





60.	From the menu on the left, select the Integrations option
 


61.	Clique em build custom extension
 

62.	Click Next
 

63.	Give a name to the extension "Auto Insurance"
64.	Enter a description
65.	Click Next
 

66.	Drag or select your skill's .json file 
67.	Click Next
 

68.	A review will be displayed 
69.	Click to expand integration details 
 

70.	All integration parameters will be displayed
 
71.	Click Finish to finish creating the extension.

 
72.	Under Extensions , find the extension that was just added.
 
73.	In the Auto Lock extension, click Add+, this action will make it accessible to be triggered in the AI Assistant Builder conversation flow
 

74.	Click Add 

 



75.	The extension is almost published, at the moment it is in Draft
76.	Click next 

 

77.	Select OAuth 2.0 authentication
78.	Click Next
 

79.	For Grant type, select password
80.	For Client ID, enter a dummy value in this product version that is not yet being validated.
81.	Client Secret file, enter a dummy value in this version of the product that is not yet being validated.
82.	In the Username field ,  enter the IBM RPA control center user
83.	In the Password  field  , enter the login password associated with the IBM RPA user
84.	In Client  Authentication, select Send as Body
85.	In the Header Prefix field, select Bearer
86.	Click Next
 
87.	Click Next
 
88.	Added the extension
 




4.20 Exercise: Creating the Conversation Flow Variables
4.21 Introduction
In this process, as the records will be collected through the AI Assistant Builder chat, we need to create the variables to use in the conversation flow, they can be created at any time, but in this document we will create them all in advance. 

Below is the layout:

Name	Guy
Name
	Free text

maritalStatus
	Free text

address
	Free text

CGCCPF
	Free text

City
	Free text

licenceDrive
	Free text

state
	Free text

age
	Free text

zipcode
	Free text

sex
	Free text

commercialUse
	Free text

emailCustomer
	Free text


4.22 Exercise Statement - Create Variables 
89.	Click Actions
 

90.	Selecione Created by you

 
91.	Clique em New Variable
 
92.	In the Name field, type the name of the first variable "name"
93.	In the Type field, select "Free Text"
94.	Click Save


 

95.	Repeat the same process for all the variables in the table from exercise 8.1, at the end of the process you will have a table like this one as an example.
 







4.23 Exercise: Creating the Conversational Flow
4.24 Introduction
Let's start our conversation flow! In this lab, we're going to take a simple route, but feel free to get creative when it comes to creating your own messages and interactions with users, or even adding new flows.

96.	Click the Ai Assistant Builder side menu in Actions.
  

97.	Clique em Create Action +
 


98.	Clique em Custom-built action

 





99.	Now, let's write a sentence that will start the flow of the conversation.
100.	Click Save 
Note: In this lab, we'll only create one trigger phrase, but you can create multiple phrases that identify the desired scenario and start the flow of the conversation. In this example, the sentence that starts the flow is "I'd like to start an insurance quote"
 





101.	Let's write the first question for the user  
102.	Haga clic Define customer response
 
Note:  In this lab we will explore the options of Options and Free Text .
103.	Select the Free text response type. 
104.	Preview that the response type has been set to "User enters free text" 




105.	In the And then  we'll select an action step, click Continue to next step 
 
106.	Click New Step to create the following user interaction box
 

107.	Enter the second question for the user "What is your current filing status?"

Note: The Front End that receives the insurance quote request accepts only two values as a response: "Married" and "Single". However, in the flow of the conversation, we will ask the question in Spanish to ensure correct understanding by the user. Because the response should be restricted to these two values, instead of allowing the user to type freely, we'll configure the flow to select the response from the predefined options.
 
108.	Under Define Customer Response, select the Options option

 

109.	Enter the first option for the "Married" user
110.	Enter the second option for the user "Single"
111.	Click Apply  
 

112.	Both options have been defined for the user
 
113.	Repeat the steps for all variables by typing a question to request the content of all the variables we created.

Note: The variables Marital Status, Gender, Trade Use must be of the  Option response  type  listed below and which follows the layout that the front-end agrees to receive as values.



Variable Name	Amounts received
Marital status	Single or Married
Sex	Male or female
Commercial Use	Yes or no
The other variables are of the Free Text type


Note: The following table contains the variables that should be converted into questions to ask the user.



Question	Define the customer's response
address
	Free Text 
CGCCPF
	Free Text
city
	Free Text
licenceDrive
	Free Text
state
	Free Text
age
	Free Text
Zip code
	Option "Casado" o "Soltero"

sex
	Option "Female" or "Male"

Commercial Use
	Option "Yes" or "No"

e-mailCustomer
	Free Text


Note: Now, let's map all the user-entered records through the Steps and associate them with a variable.


114.	Create a New Step
 


115.	Dentro do Step, clique em Set Variable Values
 
116.	select Set new value
 
117.	Selecione Session Variables
 





118.	Select the name variable 
 
119.	Selecione Action step variables

 

120.	Select the step that references the name variable.
 	

 
Note: Associate each variable with the step in which the user provided the answer. Make sure that all variables are correctly linked to their corresponding steps.


121.	Associating the variable with the passage of the conversation flow, in the end you will have this table 

 


122.	In the same step we will show all the records to the user, so that they are aware of the values written in a summary, for this we will create a text that we are starting the automation with the records.


123.	Click Insert to Variable 

 
124.	Type a message for the user and select Session Variables
 

125.	Select the name variable 

 

126.	At the end, Step will display all the variables

 
Note: The goal is to make sure that the insured sees all records clearly. Pay attention to the guidelines!




127.	Agora em And Then clique em Use na extension

 

128.	Select the Insurance Auto extension

 
129.	Operations: Select the option that appears with your nameAutoInsurance
 

130.	All parameters will be loaded and must be associated with the corresponding question in the Step. The process is similar to that of creating the Step that shows all the variables to the user. The focus is now on ensuring that this correlation allows the API to send parameters correctly to Watsonx Orchestrate. Always remember to select 'Action Step Variable'

 
 

131.	Click Apply 
 


 




132.	Create the last step to inform the user that processing is complete.

 


133.	Enter a message indicating that the quotation process has been completed

 




134.	And end the conversation flow by selecting And then = End Action

 


135.	Click Save at the top right.

 
4.25 Exercise: Final Test
4.26 Introduction
Now, let's run the conversation flow in the Watsonx Orchestrate test environment and interact with AI Assistant Builder. At the end of this interaction, the process should be completed.
4.27 Exercise Instruction
136.	Click Preview

 




137.	Type the message that starts the conversation flow: "I'd like to start an insurance quote"
 

Note: You can create as many triggers as you want by clicking the first box in the conversation flow and entering the new triggers.
  
138.	The conversation flow will start
139.	Complete the chat interaction
140.	At the end of the chat interaction, AI Assistant Builder will activate the Watsonx Orchestrate skill, which in turn will activate IBM RPA. You will see the insurance interface displayed and the quote records completed in the system. At the end of the process, an email confirming the request will be sent

Note: Running IBM RPA will interrupt the session.
4.28 Exercise: Implementing AI Assistant and Builder
4.29 Introduction
After all the necessary testing and adjustments, we are ready to implement AI Assistant Builder on our customer's system. The main systems on which Watson Orchestrate's AI Assistant Builder can be deployed are:
1.	Web Applications
2.	Mobile Apps
3.	Internal Systems
4.	Messaging platforms
5.	Virtual assistants
6.	Customer Service Portals
7.	E-commerce environments

4.30 Exercise Instruction
141.	Click Publish in the AI Assistant Builder sidebar.



 


142.	Click Publish
 



143.	Enter a description and select live as the environment

 







144.	A message of success should be displayed.
 


145.	Click Environments  in the left sidebar.

 

146.	Click Live  
 

147.	Click on web chat
 

148.	Chat Customization

 

Note: In this laboratory we will not customize for time reasons.



149.	Click Embed
 


150.	Click Copy to clipboard to copy the content.

 
 


151.	Click Close
 

152.	Edit the index.html file in the path C:\Tech Jam 2024\webAppTechJam

 

153.	Enter the code inside the body tag



 


154.	The wizard will be available on your html page. 



 




Thank you for completing this lab
