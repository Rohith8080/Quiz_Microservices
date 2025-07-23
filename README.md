  A microservice which handles login, authentication, questions, quiz, etc each as a separate service.


  --each service has it's own database.
  --one service communicates with other using feign client to fetch data from other service
  --feign client is depended on eureka.Here eureka means a server registry which has all registered instances(services running on diff ports).
  --so with help of eureka, feign client fetch data.
  --instead of using diff ports for fetching data from services, we can use api gateway,which
    means it is a reverse proxy server which forwards the incoming req from client to the appropriate service
    with help of eureka server.
