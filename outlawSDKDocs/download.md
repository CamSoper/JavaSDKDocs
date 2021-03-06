---
title: Azure development for Java | Microsoft Docs
description: Learn how to download the Azure SDK for Java, with sample code provided for Maven projects.
services: ''
documentationcenter: java
author: routlaw
manager: douge
editor: ''

ms.assetid: 4b8f8fe6-1b26-4bb4-9be9-6ae757a59e66
ms.service: multiple
ms.workload: na
ms.tgt_pltfrm: multiple
ms.devlang: Java
ms.topic: article
ms.date: 12/22/2016
ms.author: routlaw;asirveda

---
# Azure development for Java 

Use the libraries in the Java SDK for Azure to manage and use Azure services in your applications.  
   
For an overview of Azure and Java, visit the [Java developer center for Azure](https://azure.microsoft.com/en-us/develop/java).

## Installation

### Maven

Add a dependency entry in your pom.xml to add a library from the SDK to your [Maven](https://maven.apache.org) project.

For example, to include the latest version of the Azure Management SDK for Java:

```XML
<dependency>
    <groupId>com.microsoft.azure</groupId>
    <artifactId>azure</artifactId>
    <version>1.0.0-beta5</version>
</dependency>
``` 
### Gradle

Create an entry in the dependency section of your build.gradle file to add a library from the SDK to your [Gradle](https://gradle.org) project.

```
dependencies {
    compile 'com.microsoft.azure:azure:1.0.0-beta5'
}
```

## Azure service SDKs

These libraries help you integrate Azure services into your Java applications.

### [Azure Storage](https://docs.microsoft.com/azure/storage/storage-introduction)  

Data storage and messaging for your applications.

```XML
<dependency>
    <groupId>com.microsoft.azure</groupId>
    <artifactId>azure-storage</artifactId>
    <version>5.0.0</version>
</dependency>
```   

[Reference](http://azure.github.io/azure-storage-java/) | [Samples](https://github.com/Azure/azure-storage-java/tree/master/microsoft-azure-storage-samples/src/com/microsoft/azure/storage) | [GitHub](https://github.com/Azure/azure-storage-java)  


### [SQL Database](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-technical-overview)

JDBC driver for Azure SQL database.

```XML
<dependency>
    <groupId>com.microsoft.sqlserver</groupId>
    <artifactId>mssql-jdbc</artifactId>
    <version>6.1.0.jre8</version>
</dependency>
```

[Reference](https://docs.microsoft.com/en-us/sql/connect/jdbc/reference/jdbc-driver-api-reference) | [Samples](https://docs.microsoft.com/en-us/sql/connect/jdbc/step-3-proof-of-concept-connecting-to-sql-using-java) | [GitHub](https://github.com/Microsoft/mssql-jdbc)  

### [Redis Cache](https://azure.microsoft.com/en-us/services/cache/)

Low-latency, high-performance distributed key-value store.

```XML
<dependency>
    <groupId>redis.clients</groupId>
    <artifactId>jedis</artifactId>
    <version>2.9.0</version>
    <type>jar</type>
    <scope>compile</scope>
</dependency>
```   

[Reference](http://xetorthio.github.io/jedis) | [Sample](https://docs.microsoft.com/en-us/azure/redis-cache/cache-java-get-started) | [GitHub](https://github.com/xetorthio/jedis)    

### [DocumentDB](https://docs.microsoft.com/azure/documentdb/documentdb-introduction)

Scalable NoSQL database with JSON documents and SQL or JavaScript query syntax.   

```XML
<dependency>
    <groupId>com.microsoft.azure</groupId>
    <artifactId>azure-documentdb</artifactId>
    <version>1.9.3</version>
</dependency>
```

[Reference](http://azure.github.io/azure-documentdb-java/) | [Samples](https://docs.microsoft.com/en-us/azure/documentdb/documentdb-java-application) | [GitHub](https://github.com/Azure/azure-documentdb-java)   

### [Service Bus](https://docs.microsoft.com/en-us/azure/service-bus-messaging/service-bus-fundamentals-hybrid-solutions)

Java Messaging Support (JMS) through [AMQP](https://en.wikipedia.org/wiki/Advanced_Message_Queuing_Protocol) to connect your applications.

```XML
<dependency>
  <groupId>org.apache.qpid</groupId>
  <artifactId>qpid-jms-client</artifactId>
  <version>0.11.1</version>
</dependency>
```

[Reference](http://docs.oracle.com/javaee/7/api/javax/jms/package-summary.html) | [Sample](https://github.com/apache/qpid-jms/tree/0.20.0/qpid-jms-examples) | [GitHub](https://github.com/apache/qpid-jms)    

### [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-whatis)   

Identity management and secure sign-in for your applications.

```XML
<dependency>
    <groupId>com.microsoft.azure</groupId>
    <artifactId>adal4j</artifactId>
    <version>1.1.3</version>
</dependency>
```
   
[Reference](https://github.com/AzureAD/azure-activedirectory-library-for-java) | [Samples](https://github.com/Azure-Samples?utf8=%E2%9C%93&q=active%20directory%20&type=&language=java) | [GitHub](https://github.com/AzureAD/azure-activedirectory-library-for-java) 
 
### [Key Vault](https://docs.microsoft.com/azure/key-vault) 

Encrypt secrets and keys and safely access them from your applications. 

```XML
<dependency>
    <groupId>com.microsoft.azure</groupId>
    <artifactId>azure-keyvault</artifactId>
    <version>1.0.0-beta3</version>
</dependency>
```

[Reference](https://docs.microsoft.com/en-us/java/api/com.microsoft.azure.keyvault) | [Samples](https://github.com/Azure-Samples/batch-keyvault-java-management) | [GitHub](https://github.com/Azure/azure-sdk-for-java)  

### [Event Hub](https://docs.microsoft.com/en-us/azure/event-hubs/event-hubs-what-is-event-hubs) 
   
High throughput event and telemetry ingestion for your instrumentation or IoT scenarios.

```XML
<dependency> 
    <groupId>com.microsoft.azure</groupId> 
    <artifactId>azure-eventhubs</artifactId> 
    <version>0.10.0</version> 
</dependency>   
```

[Reference](https://docs.microsoft.com/en-us/java/api/com.microsoft.azure.eventhubs) | [Samples](https://github.com/azure/azure-event-hubs-java#publishing-events) | [GitHub](https://github.com/azure/azure-event-hubs-java)   

### [IoT Service](https://docs.microsoft.com/azure/iot-hub/)

- Create/remove/update/list device identities in your IoT hub
- Send messages to your devices and get feedback when they're delivered

```XML
<dependency>
    <groupId>com.microsoft.azure.sdk.iot</groupId>
    <artifactId>iot-service-client</artifactId>
    <version>1.0.13</version>
</dependency>
```   
   
[Reference](http://azure.github.io/azure-iot-sdks/java/service/api_reference/index.html) | [Samples](https://github.com/Azure/azure-iot-sdk-java/tree/master/service/iot-service-samples) | [GitHub](https://github.com/Azure/azure-iot-sdk-java) 

### [IoT Device](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide)

Send a message to an IoT hub from your device.  

```XML
<dependency>
    <groupId>com.microsoft.azure.sdk.iot</groupId>
    <artifactId>iot-service-client</artifactId>
    <version>1.0.18</version>
</dependency>
```  

[Reference](http://azure.github.io/azure-iot-sdks/java/device/api_reference/index.html) | [Samples](https://github.com/Azure/azure-iot-sdk-java/tree/master/device/iot-device-samples) | [GitHub](https://github.com/Azure/azure-iot-sdk-java) 

### [Data Lake Store](https://docs.microsoft.com/azure/data-lake-store/data-lake-store-overview)   
   
Capture data of any size in a single location for performing data analytics.    

```XML
<dependency>
   <groupId>com.microsoft.azure</groupId>
   <artifactId>azure-data-lake-store-sdk</artifactId>
   <version>2.1.4</version>
</dependency>
```   

[Reference](https://azure.github.io/azure-data-lake-store-java/javadoc/) | [Samples](https://github.com/Azure-Samples/data-lake-store-java-upload-download-get-started) | [GitHub](test.md) 

### [AppInsights](https://docs.microsoft.com/azure/application-insights/app-insights-overview)

- Track usage of web applications
- Capture logs and correlate events with page views and requests
- Add custom telemetry
- Monitor application availability

```XML
<dependency>
    <groupId>com.microsoft.azure</groupId>
    <artifactId>applicationinsights-web</artifactId>
    <version>1.0.7</version>
</dependency>
```

[Reference](https://docs.microsoft.com/en-us/java/api/com.microsoft.applicationinsights) | [Samples](https://docs.microsoft.com/en-us/azure/application-insights/app-insights-java-get-started) | [GitHub](https://github.com/Microsoft/ApplicationInsights-Java) 



## Azure resource management

The [Azure Management Libraries for Java](https://github.com/Azure/azure-sdk-for-java) lets you create and manage your Azure resources. 

Add the Azure resource management libraries for Java to your project with the following Maven dependency:

```XML
<dependency>
    <groupId>com.microsoft.azure</groupId>
    <artifactId>azure</artifactId>
    <version>1.0.0-beta5</version>
</dependency>
```

For a list of currently supported resources, sample code, and help on getting started with the API, see the [project readme on Github](https://github.com/Azure/azure-sdk-for-java).

## See Also
For more information about the Azure Toolkits for Java IDEs, see the following links:

* [Azure Toolkit for Eclipse]
  * [Installing the Azure Toolkit for Eclipse]
  * [Create a Hello World Web App for Azure in Eclipse]
  * [What's New in the Azure Toolkit for Eclipse]
* [Azure Toolkit for IntelliJ]
  * [Installing the Azure Toolkit for IntelliJ]
  * [Create a Hello World Web App for Azure in IntelliJ]
  * [What's New in the Azure Toolkit for IntelliJ]

For more information about using Azure with Java, see the [Azure Java Developer Center].

> [!NOTE]
> For detailed information on setting up build paths in Eclipse, see the [Java Build Path] article at the Eclipse website.
>

<!-- URL List -->

[Azure Toolkit for Eclipse]: ./azure-toolkit-for-eclipse.md
[Azure Toolkit for IntelliJ]: ./azure-toolkit-for-intellij.md
[Create a Hello World Web App for Azure in Eclipse]: ./app-service-web/app-service-web-eclipse-create-hello-world-web-app.md
[Create a Hello World Web App for Azure in IntelliJ]: ./app-service-web/app-service-web-intellij-create-hello-world-web-app.md
[Installing the Azure Toolkit for Eclipse]: ./azure-toolkit-for-eclipse-installation.md
[Installing the Azure Toolkit for IntelliJ]: ./azure-toolkit-for-intellij-installation.md
[What's New in the Azure Toolkit for Eclipse]: ./azure-toolkit-for-eclipse-whats-new.md
[What's New in the Azure Toolkit for IntelliJ]: ./azure-toolkit-for-intellij-whats-new.md

[Azure Java Developer Center]: http://go.microsoft.com/fwlink/?LinkID=699547
[Azure Libraries Repository on Maven]: http://go.microsoft.com/fwlink/?LinkID=286274
[Java Build Path]: http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.jdt.doc.user%2Freference%2Fref-properties-build-path.htm
[license]: http://www.apache.org/licenses/LICENSE-2.0.html
[maven-getting-started]: http://go.microsoft.com/fwlink/?LinkID=622998