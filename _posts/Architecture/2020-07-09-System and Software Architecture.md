# Cost Analyser Application -- System and Software Architecture




**Develop a simple architecture model for your use case!**


![Architekturmodell](/cost-analyzer-ilv/images/Architektur_Modell.png)


**Which architecture would you choose and why?**

We decided us for the microservice architecture. We think, that this architecture can deliver desired value for our application. Furthermore they appear to be clear. As you can see in the figure above our architecture is quite simple. We want to offer two services to our customers with our application. First, to show the movements of their money. The second service is the possibility to evaluate his data simple and effektively (uploading services + analytical services). We think that for our goals the shown microservice architecture is suitable.

**Which kind of interfaces are neccessary? Which desireable and which possible to implement?**

For our project we decided us to use the REST API interface. Alternatively SOAP and WDL can be used. The usage of REST API offers the possibility of a good scalability as client and server are far apart. Another advantage is to integrate is easily into a web site without changing its infrastructure.

**How can we use messaging?**

Asynchrone messaging can be used at the analytical applications when a customer requests a new analysis that needs to train a more complex model. This request can be stored in a queue and implemented at a fitting time point.

**Which information can be extracted out of log files?**

In our use case we would like to extract timestamps of uploads, the bank names and from the user using the application. Furthermore all kinds of errors while the usage should be logged. We also need to know by loggin when we receive requests by our customers and the time when he received the answer. Good to know would be also the usage in form of numbers of logins and the duration he spends on the platform.

**How could you stumble over internationalization - Not only because of customers of different countries?**

We think that we are prepared well in this topic as our requirements are defined aswell well. Theoretically we can imagine following issues (In the first step our application is avaulable in the DACH area and GB + USA):

- Different legal requirements
- Different currencies
- Different time zones
- Metric systems with different formats
- unknown letters (wrong character set)
