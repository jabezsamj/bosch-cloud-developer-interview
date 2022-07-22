# bosch-cloud-developer-interview




Cloud Service Developer_COB_ETP_2022


Interview level 1 - Programming task


Scenario : 

AWS provides IOT core service which helps to connect and manage millions of devices at ease. Generally, IOT edge devices connect to the backend servers though MQTT protocol. 

Provisioning a device (Onboarding IoT devices into a fleet) is a major task in getting the IoT devices up and running. It is important that the process is secure and is seamless.  Fleet-provisioning service in AWS-IOT core provides this process as an out of the box solution. 

There are two stages : 

Stage 1 (Production unit) : When the complete fleet of devices are produced at the production unit. We can save device related information, which we can save it in our Database and use it for verifying when the devices gets onboarded from the customer premise at a later stage.


Stage 2 (Customer premise) : 

When the individual devices are taken to the customer premise and they connect to internet for the first time. The devices are onboarded. IoT core will take care of this.





**Task** :  

Create a REST-api endpoint which can receive device related information


Create a API-gateway with a WAF infront of it. Create a POST request method in the API-gateway. The API-gateway should be connected to a Lambda function. The lambda function should receive the payload from the REST api call and place it in a DynamoDB database.

The payload is Serial-number of the produced device.
The production unit will call this api for every device that is produced in the unit, to save device related information for future verification.


**Architecture**

![image](https://github.com/jabezsamj/bosch-cloud-developer-interview/blob/main/interview_task.png)
