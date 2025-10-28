# lab-4-sentence-danim

This is a Spring Cloud Eureka client project that is registered and discovered in the **lab-4-eureka-server-danim** and uses other registered client projects **lab-4-subject, lab-4-verb, lab-4-article, lab-4-adjective and lab-4-noun** to mount a sentence.

# Starting this client repository

The steps to used it are:
- Start the **lab-4-eureka-server-danim** repo and check it's started correctly in http://localhost:8010
- Start the rest of client services ([See README from lab-4-eureka-server-danim](https://github.com/dlmogft/lab-4-eureka-server-danim/blob/main/README.md))
- Start the class annotated with @SpringBootApplication
- Check that the sentence is shown in the URL http://localhost:8020/sentence

# Dependencies

Eureka Discovery Client, Config Server (if uses Spring Cloud Config)

# Tips

- The project starting class is annotated with **@SpringBootApplication** and also with @EnableDiscoveryClient to indicate that acts as an Eureka Client
- The **application.yml** config file specifies the URI of the Eureka Server repo **lab-4-eureka-server-danim**. If the project also uses the Spring Cloud Config feature, it specified instead the URI of the Git repository where the configuration files are stored, **spring-cloud-server-config-danim** and also the profile to read the correct **application-<profile>.yml** file from this Git repository.
- The **SentenceRestController** has a **DiscoveryClient** autowired instance that is used to load the **ServiceInstance**'s from the clients **lab-4-subject, lab-4-verb, lab-4-article, lab-4-adjective and lab-4-noun** that are used to get a word from every service client and mount tte sentence
