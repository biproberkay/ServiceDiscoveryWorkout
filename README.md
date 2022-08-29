# ServiceDiscoveryWorkout
I created this repository to save my progress about understanding Service Discovery concept. Let get started.

- i need a case📌
- it looks like a subtopic of **[Microservice Architecture](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#workingofmicroservices)**
- Service Discovery –> A guide to find the route of communication between microservices.[¹][1]
## Keywords
Eureka, Service Registry, API Gateway, Clients, Identity Providers
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
## Refrences
- [gencay yıldız blog](https://www.gencayyildiz.com/blog/netflix-eureka-server-ile-service-discovery/)

[1]: https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#workingofmicroservices:~:text=Service%20Discovery%C2%A0%E2%80%93%20A%20guide%20to%20find%20the%20route%20of%20communication%20between%20microservices "tanım"