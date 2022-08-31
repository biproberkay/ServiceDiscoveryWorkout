# ServiceDiscoveryWorkout
I created this repository to save my progress about understanding Service Discovery concept. Let get started.

- i need a case📌
- it looks like a subtopic of **[Microservice Architecture](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#workingofmicroservices)**
- Service Discovery –> A guide to find the route of communication between microservices.[¹][1]
- Why Do Microservices Need an API Gateway?[🔗][2]
## Keywords
Eureka, Service Registry, API Gateway, Clients, Identity Providers, Consul, Ocelot[¹][1],OpenId
## Samples
### [Sample 1](Samples/Eureka-Service-Discovery-Example-master/README.md) 
in this sample. there is 3 csprojects communicates eachother. AService, BService, CService. this is a basic example with Netflix Eureka. 2 of them i,s API and one for console project. 

<!-- TODO: Commit -->
<!-- TODO: research new example -->
### [Sample 2](Samples/Ocelot.Gateway.Eureka.ServiceDiscovery.Demo-main/README.md)
Service discovery with eureka is used via an api gateway with ocelot. 
<!-- I need an example whic implements also authentication with api gateway and service discovery -->

## articles
### [Microservice Mimarilerinde Service Discovery](https://medium.com/i%CC%87yi-programlama/microservice-mimarilerinde-service-discovery-7a6ebceb1b2a)
📌2 tür service discovery patterni bulunmakta.Client-Side Service Discovery ve Server-Side Service Discovery.


## Notes
`builder.Services.AddDiscoveryClient(builder.Configuration);`

[Steeltoe.Discovery.Eureka](https://www.nuget.org/packages/Steeltoe.Discovery.Eureka/)
appsettingsjson
```

  "spring": {
    "application": {
      "name": "AService"
    }
  },
  "eureka": {
    "client": {
      "serviceUrl": "http://localhost:8761/eureka/",
      "shouldFetchRegistry": "true",
      "shouldRegisterWithEureka": true,
      "validateCertificates": false
    },
    "instance": {
      "port": "7175",
      "ipAddress": "localhost",
      "preferIpAddress": true
    }
  }
  
  ```
 >[26:15](https://docs.microsoft.com/en-us/shows/on-net/service-discovery-with-steeltoe#time=26m15s) - Discovery sfirst strategy is something that's very commonly used in java and spring worlds.

## Refrences
- [gencay yıldız blog](https://www.gencayyildiz.com/blog/netflix-eureka-server-ile-service-discovery/)

- [Service Discovery with Steeltoe](https://docs.microsoft.com/en-us/shows/on-net/service-discovery-with-steeltoe#time%3D04m08s)

[1]: https://docs.microsoft.com/en-us/dotnet/architecture/microservices/multi-container-microservice-net-applications/implement-api-gateways-with-ocelot "Ocelot is a .NET API Gateway. This project is aimed at people using .NET running a micro services / service oriented architecture that need a unified point of entry into their system. However it will work with anything that speaks HTTP and run on any platform that ASP.NET Core supports."
[2]: https://konghq.com/learning-center/api-gateway/why-microservices-need-api-gateway#:~:text=Authentication%2C%20Authorization%2C%20and%20Audit "The API Gateway can perform the authentication itself or use external authentication providers for that task."