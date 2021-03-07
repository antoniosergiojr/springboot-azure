## Spring Boot no Azure | [Aceleração Global Dev #6 Avanade](https://digitalinnovation.one/)

Example of a web project using Spring Boot on Azure.

## 📌 Index
- ⚙ [Settings](#-settings)
- 💻 [Technologies](#-technologies)
- 🚀 [How to run](#-how-to-run)
---

## ⚙ Settings
  Have a microsoft azure [account](https://azure.microsoft.com/pt-br/free/), set up following the [steps](https://docs.microsoft.com/en-us/azure/developer/java/spring-framework/configure-spring-data-mongodb-with-cosmos-db) and watch the [video](https://youtu.be/rSWbDk1yAME) tutorial.

---

## 💻 Technologies
    - Java
    - Spring Boot
    - Maven
    - WebFlux (working reactively in spring and Netty embedded server)
    - Microsoft Azure (CosmosDB with the MongoDB API)    
---

## 🚀 How to run

  > Cloning the repository
  ```bash
    # Cloning repository
    git clone https://github.com/antoniosergiojr/springboot-azure.git
  ```

  > Running web project
  ```bash
    # Accessing web project
    cd springboot-azure

    # Running web project
    mvn azure-webapp:config
    -Define value for OS [Linux]
    -Define value for pricingTier [P1v2]
    -Define value for javaVersion [Java 11]
    
    mvn azure-webapp:config
    -Please choose which part to config [Application]
    -Define value for appname [springboot-1613]
    -Define value for resourceGroup [springboot-1613-rg]: azure-springboot
    -Define value for region [westeurope]: central-us
    
    mvn clean package
    mvn azure-webapp:deploy
    
    run application and then access: 
    http://localhost:8080/users
    http://localhost:8080/users/webflux
    
  ```
---
