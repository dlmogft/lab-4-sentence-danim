# lab-4-sentence-danim

This is a Spring Cloud Eureka client project that is registered and discovered in the **lab-4-eureka-server-danim** and uses other registered client projects **lab-4-subject, lab-4-verb, lab-4-article, lab-4-adjective and lab-4-noun** to mount a sentence.

# Starting this client repository

The steps to used it are:
- Start the **lab-4-eureka-server-danim** repo and check it's started correctly in http://localhost:8010
- Start the rest of client services ([See README from lab-4-eureka-server-danim](https://github.com/dlmogft/lab-4-eureka-server-danim/blob/main/README.md))
- Start the class annotated with @SpringBootApplication
- Check that the sentence is shown in the URL http://localhost:8020/sentence
