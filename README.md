# UDM-UDR

**Stateless Design**<br />
If an application and design in a way that the application logic is handled by the application entirely and that data lies entirely outside of the application function. Then it is called as stateless design. So we need to keep data, entirely decouples from the application logic.

**UDR**<br />
It is the database where various type of data is stored. In this we have four major kind of data as follows

1. Subscription Data: It refers to the data about all the subscribers and what kind of subscription they have, what type of network slice they can access, what applications services that particular subscriber can access.

2. Policy Data:  This holds policy related all the policy related information like which application need will be prioritized and which needs to be treated differently in the quality of services mechanism, which geographical areas does a certain device have access to and etc. Here all the policy related information store that we saw in the PCF.

3. Structure Data for Exposure: There are some data data is stored in a particular design that it can be exposed to the third party application, which are running on top of the 5G system to provide advanced features to store some information and provide access to another application. Then that data are also stored in the UDR. The exposure function is itself provided by the function called Network Exposure Function (NEF).

4. Application Data: Some third pary application can also store their necessary data in the UDR.

**UDM**

In order to make date out of the UDR, we need to have an interface towards UDR. All essentials functions like AMF,SMF etc, to access the data available through IDR. So you UDM is the front end for the user subscription data stored in the UDR. It provides an interface using which AMF,SMF etc can access the data provided and stored in the UDR. But PCF can directly access the data restored in the UDR, particularly the policy data. And then, when a different application function want to access the data. They use the services provided by the network exposure function or NEF who access the data that is stored in the UDR. Who summarize it can be seen that the UDM is front end and being front end it supports by hosting the application logic for access management, registration management and authentication management.

**UDM Services**

i) Nudm_SubscriberDataManagement
This is used by the network functions to retrieve subscription data from the UDM.

- Nudm_SDM_Get
	this is used by the consumer network functions to retrieve subscriber data

- Nudm_SDM_Notification
	this is used by the UDM to notify network function consumer of update of previous retrieved subscriber data

- Nudm_SDM_Subscriber
	this is used by the network functions (such as AMF, SMF) who subscribe update of UE subscriber data

- Nudm_SDM_Unsubscribe
	this is used by the network function example AMF and SMF to unsubscribe to further notification

- Nudm_SDM_Info
	this is used by the AMF to provide UDM with status information regarding subscription data management procedures toward the UE

ii) Nudm_UEContextManagement
This is used to manage the registration of serving network function with you UDM

- Nudm_UECM_Registration
	This is used to register at udm as the network function serving the UE

- Nudm_UECM_Deregistration
	this is used by the previously register network functions such as AMF SMF to deregister from the UDM

- Nudm_UECM_DeregistrationNotification
	this is used by the udm to notify an AMF said it has been deregistered as serving network function for a UE

- Nudm_UECM_Get
	this is used by the network function to retrieve registration information from udm

- Nudm_UECM_Update
	this is used by the registered network function to update the stored registration information

iii) Nudm_UEAuthentication
This is used by the AUSF to get authentication and provide you UDM with the result of the authentication procedure success

- Nudm_UEAuthentication_Get
	this is used by the AUSF to retrieve authentication data from udm

- Nudm_UEAuthentication_ResultConfirmation
	this is used by the AUSF to inform about the result of an authentication procedure with a UE

iv) Nudm_EventExposure
It allows the network exposure function to subscribe, unsubscribe and get notified about the events from the UDM

- Nudm_EE_Subscribe
	this allows the network function to subscribe or to update event subscription

- Nudm_EE_Unsubscribe
	this allows the network exposure function to delete the subscription to event in UDM that is previously subscribed to

- Nudm_EE_Notify
	this is used by the UDm to report on events that was previously subscribed by the network exposure function

v) Nudm_ParameterProvision
this allows the network function or rather application function via network exposure function for provisioning of an information. Example: expected UE behavior, network configuration parameters.
