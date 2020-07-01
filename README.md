# Spring-Feign

Feign is a rest service client it makes it easy to call restful web services, when we use resttemplate to call the services,
it was really a complex to write a lot of complex code, unnecessary duplicate to talk to restful service

with feign follow the steps
1. add a dependency 
2.@EnableFeignClients("packaage name") - to scan for clients - put it in the main class 
3.create a simple proxy 
4.Annotate with class level @FeignClient(name="spring.application.name",url="localhost:8081") 
  spring.application.name - name of the service which we are going to call 
	url - is the one which we are going to talk to
5.copy the same definition which is available in other service and paste in proxy class
6.able to use that proxy to make the call to the service
7.Utilize the proxy in the conteller with the help of Dependnecy Injection @Autowired 
8.feign helps us to simplify the client code to talk restful web service

ex: if the currency-exchange-service is offering a 15 services all the details of how to talk to external service would be present
just in one place which is inside the proxy class

just call the method on the proxy and get the details back.

whenever using exactly speicify the path variable
