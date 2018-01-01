# Tareas Lab 6

###Two microservices running and registered

* Account service running
![](images/port2222.png)
![](images/accounts server web.png)
* Web service running
![](images/webserver.png)
![](images/web server web.png)

###Service registration has the two microservices registered
![](images/registration.png)
![](images/1 registered.png)

###Second account microservice running in port 4444 and registered
![](images/port4444.png)
![](images/2 registered.png)

###What happens when you kill the microservice with port 2222? Can the web service provide information about the accounts? Why?
When the account server (port:2222) is killed and the web server attempts to provide information about the accounts, it returns a Connection Refused error because the port is inactive. When the web server tries to connect again, it will ask the Registration server to obtain the valid Account server addres. It gets the correct account server (port:4444) and it is able to return the information.