# UDM-UDR

**Stateless Design**<br />
If an application and design in a way that the application logic is handled by the application entirely and that data lies entirely outside of the application function. Then it is called as stateless design. So we need to keep data, entirely decouples from the application logic.

**UDR**<br />
It is the database where various type of data is stored. In this we have four major kind of data as follows

1. Subscription Data: It refers to the data about all the subscribers and what kind of subscription they have, what type of network slice they can access, what applications services that particular subscriber can access.

2. Policy Data:  This holds policy related all the policy related information like which application need will be prioritized and which needs to be treated differently in the quality of services mechanism, which geographical areas does a certain device have access to and etc. Here all the policy related information store that we saw in the PCF.

3. Structure Data for Exposure: There are some data data is stored in a particular design that it can be exposed to the third party application, which are running on top of the 5G system to provide advanced features to store some information and provide access to another application. Then that data are also stored in the UDR. The exposure function is itself provided by the function called Network Exposure Function (NEF).

4. Application Data: Some third pary application can also store their necessary data in the UDR.
