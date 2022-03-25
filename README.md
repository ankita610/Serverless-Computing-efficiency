## Serverless Architecture
Cloud Computing Coursework              

Ankita Tripathy

### Chapter 1 : Introduction

#### 1.1 Context
Serverless Computing is a service that allows code to be triggered without the requirement of a physical platform to do so. It provides a cloud based architecture for the code to run. The code is triggered on demand without the explicit need of storing it on a server. Azure Function Apps provides us with a functionality where in we can directly write our code on the portal and can also use various triggers such as HTTP Trigger, Time Trigger, Event Trigger, etc.

Azure Function Apps is a service (Open Service) to run small pieces of code on the cloud system. This runs on Pay-per-use model which is an extension of the Azure App Service. Not only do they support multiple languages including but not limited to C#, Java, Python, Powershell but also supports integrated security services. Pieces of code hosted on the cloud can also be integrated with external tools. Additionally, integration with GitHub, DevOps is also supported.

To run a function app, we would need a trigger where it would run the code in order to produce an output. A function has only one trigger but can have multiple inputs and outputs. Since the model pricing is based on its use, major disadvantages to server less computing include accidental overload, lack of operational tools, limited API resources.


### Chapter 2: The Paradigm

#### 2.1 Server based computing vs. Serverless computing
Server based computing typically follows a 3 tier architecture consisting of a database layer, application layer and presentation layer where as server less computing follows a similar architecture in the form of micro services in the application layer and is independent of a physical infrastructure and hosted on the cloud. To be able to perform server based computing one would have to follow various installations and setup which could potentially take up a lot of space where as serverless computing allows a functionality to develop functions on web.

<img width="331" alt="image" src="https://user-images.githubusercontent.com/25227772/160115883-667a0265-1059-432e-b7e4-3e5701481e95.png">

Fig 2a : What triggers a function app?

<img width="406" alt="image" src="https://user-images.githubusercontent.com/25227772/160115964-a76dc99e-c396-4f8b-9e41-1b9fc658ef84.png">

Fig 2b: Architecture: Server based computing

#### 2.2 Commercial use : Serverless Computing
Aside from the now established fact that Serverless Computing requires zero servers, operating systems or related software/hardware, one of the major benefits it has to provide is the built in high availability and fault tolerance irrespective of the scale of business. 
The serverless, infrastructure independent architecture provides the option to a developer to execute their scripts and code as and when required. Serverless functions are triggered on specific events based on the kind of function triggers allocated.

<img width="554" alt="image" src="https://user-images.githubusercontent.com/25227772/160116004-cf380700-9173-4878-b1e1-861fa17c7cd0.png">

Fig 2c: Serverless model and its functionalities

Choosing to work with Function As A Service (FanS) would be helpful to a commercial entity because of its sheer ease of development and integration with an existing or a new CI/CD pipeline. Transitioning from one cloud service to another is also not a complex process which could pose to be an easy trump for anybody willing to switch to a serverless model.
In its best, business applications to Cloud computing include
Integration with IDEs and IoT based devices including circuits, sensors, phones, etc.
Serverless structure enabling no idle capacity cuts back on latency and enables cost effective solutions.
A piece of code and its resources on the cloud can be scaled up and down as and when required and provides for a comfortable mode of deployment that is hassle free and easy for a novice.


### Chapter 3: Experimental Design

#### 3.1 Function Apps
To compare and evaluate the performance of Azure function apps, I have created two function apps viz. sc20at and sc20atsecond. The details have been tabulated below : 

<img width="554" alt="image" src="https://user-images.githubusercontent.com/25227772/160116113-2f9a7067-1a57-45a1-87ca-310aaf6a7a74.png">

<img width="553" alt="image" src="https://user-images.githubusercontent.com/25227772/160116169-41ab2302-37da-497e-902f-42049da21fff.png">

Fig 3a: Function app url : sc20at

<img width="553" alt="image" src="https://user-images.githubusercontent.com/25227772/160116195-9c8d2c5d-d409-42a8-88f4-85e7efbafa4d.png">

Fig 3b: Function app url : sc20atsecond

#### 3.2 Function Apps - Output
#### 3.2.1 Function App : sc20at

<img width="553" alt="image" src="https://user-images.githubusercontent.com/25227772/160116399-b56a03f5-ca68-4ef5-af36-871dc67b5c52.png">

Fig 3c: HTTPTrigger function to print the factorial of 10 triggered using the function URL.

<img width="551" alt="image" src="https://user-images.githubusercontent.com/25227772/160116708-573d432f-c0b7-4efa-8a86-628977c9ab49.png">

Fig 3d: HTTPTrigger function tested on the Azure Web Portal to prints the factorial of 10

<img width="553" alt="image" src="https://user-images.githubusercontent.com/25227772/160116444-d7d289da-ea7f-449a-80e7-209589fddabe.png">

Fig 3e: HTTPTrigger function to print the count of palindromes between 1 and 2000 triggered using the function URL.

<img width="551" alt="image" src="https://user-images.githubusercontent.com/25227772/160116754-a8aecd73-5fe4-4c53-bc4c-a66af2510939.png">

Fig 3f:  HTTPTrigger function run on the Azure Web Portal to print the number of palindromes between 1 and 2000.

#### 3.2.2 Function App : sc20atsecond

<img width="553" alt="image" src="https://user-images.githubusercontent.com/25227772/160116492-72958b6b-fbff-4eec-89a7-c3858290ad35.png">

Fig 3g: HTTPTrigger function to print the factorial of 10 triggered using the function URL.

<img width="551" alt="image" src="https://user-images.githubusercontent.com/25227772/160116793-451c3be1-d42b-42c1-880a-19e3897a7dc7.png">

Fig 3h: HTTPTrigger function tested on the Azure Web Portal to print the factorial of 10

<img width="553" alt="image" src="https://user-images.githubusercontent.com/25227772/160116642-b24710fd-44fa-4a90-ba89-dea281c4dbcf.png">

Fig 3i: HTTPTrigger function to print the count of palindromes between 1 and 2000 triggered using the function URL.

<img width="556" alt="image" src="https://user-images.githubusercontent.com/25227772/160116854-9bc938e5-c8c0-49d2-a6b5-77b9434e4b49.png">

Fig 3j:  HTTPTrigger function run on the Azure Web Portal to print the number of palindromes between 1 and 2000.

### Chapter 4 : Experiment Outcome

#### 4.1 Function Execution Count
<img width="706" alt="image" src="https://user-images.githubusercontent.com/25227772/160111965-5f1f3699-f3fd-424d-9995-179d8343e607.png">

To measure the execution performance of the implementation, I wrote a python function that invoked each function 200 times by trigger the URL via a GET method. The graph depicts every the total function execution count of both the function apps to be a total of 400 each.

#### 4.2 Average Memory Working Set
<img width="716" alt="image" src="https://user-images.githubusercontent.com/25227772/160111680-ed9b0feb-202b-4f5a-aff5-520fcc8f0ac9.png">

Having invoked the functions, that follow the same algorithm and adhere to the same time and space complexity, for an equal number of 200 times each, the average memory working set reserved by each function app is of remarkable difference. The function app that uses .NET as a framework utilises almost half as much as that of node.js. This could be one of the major reasons why .NET is a supported runtime stack in all the Cloud Services present in the industry today.

#### 4.3 Data In vs Data Out
<img width="706" alt="image" src="https://user-images.githubusercontent.com/25227772/160112107-76085d50-7f72-4dcf-8365-879343419626.png">

Neither of the functions require an input per se, except for the name of the user. It is observed that the Data In value for sc20at is lower than that of sc20atsecond and the same trend has been observed in terms of Data out value. However, the ratio of Data in to Data out is similar for both the function apps. It has been observed that, there is a flux in data in and out value even when the functions have not been triggered explicit which could pose as an anomaly .

#### 4.4 Response time
<img width="706" alt="image" src="https://user-images.githubusercontent.com/25227772/160113899-4c6da6fd-c884-4877-837e-b4de85c089fe.png">

The average response time for sc20atsecond is again observed to be more than double as that of sc20at. Additionally, latency of very minimal amplitude was observed for the stack that used Node.js. Overhead experienced by both of the function apps were considerably different even though the number of triggers per function were the same. Despite the synchronous HTTP Triggers, there were minimal but prevalent latencies.

### Conclusion
Serverless computing is a technology driven solution that eradicates the woes of space and extensive server installation processes. Due to the numerous benefits, the utilisation of cloud services by commercial organisations will see a substantial increase. The performance owing to the fact that it is flexible, scalable and cost effective is an optimal solutions for organisations today in the world of space deprivation. 
