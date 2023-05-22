<img src="https://cdn.jsdelivr.net/gh/apolloconfig/apollo@master/doc/images/logo/logo-simple.png" alt="apollo-logo" width="40%">

English | [中文](https://www.apolloconfig.com/#/zh/README)

# Apollo - A reliable configuration management system

[![Build Status](https://github.com/apolloconfig/apollo/workflows/build/badge.svg)](https://github.com/apolloconfig/apollo/actions)
[![GitHub Release](https://img.shields.io/github/release/apolloconfig/apollo.svg)](https://github.com/apolloconfig/apollo/releases)
[![Maven Central Repo](https://img.shields.io/maven-central/v/com.ctrip.framework.apollo/apollo.svg)](https://mvnrepository.com/artifact/com.ctrip.framework.apollo/apollo-client)
[![codecov.io](https://codecov.io/github/apolloconfig/apollo/coverage.svg?branch=master)](https://codecov.io/github/apolloconfig/apollo?branch=master)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Apollo is a reliable configuration management system. It can centrally manage the configurations of different
applications and different clusters. It is suitable for microservice configuration management scenarios.

The server side is developed based on Spring Boot and Spring Cloud, which can simply run without the need to install
additional application containers such as Tomcat.

The Java SDK does not rely on any framework and can run in all Java runtime environments. It also has good support for
Spring/Spring Boot environments.

The .Net SDK does not rely on any framework and can run in all .Net runtime environments.

For more details of the product introduction, please
refer [Introduction to Apollo Configuration Center](https://www.apolloconfig.com/#/zh/design/apollo-introduction).

For local demo purpose, please refer [Quick Start](https://www.apolloconfig.com/#/zh/deployment/quick-start).

Demo Environment:

- [http://81.68.181.139](http://81.68.181.139/)
- User/Password: apollo/admin

# Screenshots

![Screenshot](https://cdn.jsdelivr.net/gh/apolloconfig/apollo@master/docs/en/images/apollo-home-screenshot.jpg)

# Features

* **Unified management of the configurations of different environments and different clusters**
    * Apollo provides a unified interface to centrally manage the configurations of different environments, different
      clusters, and different namespaces
    * The same codebase could have different configurations when deployed in different clusters
    * With the namespace concept, it is easy to support multiple applications to share the same configurations, while
      also allowing them to customize the configurations
    * Multiple languages is provided in user interface(currently Chinese and English)

* **Configuration changes takes effect in real time (hot release)**
    * After the user modified the configuration and released it in Apollo, the sdk will receive the latest
      configurations in real time (1 second) and notify the application

* **Release version management**
    * Every configuration releases are versioned, which is friendly to support configuration rollback

* **Grayscale release**
    * Support grayscale configuration release, for example, after clicking release, it will only take effect for some
      application instances. After a period of observation, we could push the configurations to all application
      instances if there is no problem

* **Authorization management, release approval and operation audit**
    * Great authorization mechanism is designed for applications and configurations management, and the management of
      configurations is divided into two operations: editing and publishing, therefore greatly reducing human errors
    * All operations have audit logs for easy tracking of problems

* **Client side configuration information monitoring**
    * It's very easy to see which instances are using the configurations and what versions they are using

* **Rich SDKs available**
    * Provides native sdks of Java and .Net to facilitate application integration
    * Support Spring Placeholder, Annotation and Spring Boot ConfigurationProperties for easy application use (requires
      Spring 3.1.1+)
    * Http APIs are provided, so non-Java and .Net applications can integrate conveniently
    * Rich third party sdks are also available, e.g. Golang, Python, NodeJS, PHP, C, etc

* **Open platform API**
    * Apollo itself provides a unified configuration management interface, which supports features such as
      multi-environment, multi-data center configuration management, permissions, and process governance
    * However, for the sake of versatility, Apollo will not put too many restrictions on the modification of the
      configuration, as long as it conforms to the basic format, it can be saved.
    * In our research, we found that for some users, their configurations may have more complicated formats, such as
      xml, json, and the format needs to be verified
    * There are also some users such as DAL, which not only have a specific format, but also need to verify the entered
      value before saving, such as checking whether the database, username and password match
    * For this type of application, Apollo allows the application to modify and release configurations through open
      APIs, which has great authorization and permission control mechanism built in

* **Simple deployment**
    * As an infrastructure service, the configuration center has very high availability requirements, which forces
      Apollo to rely on external dependencies as little as possible
    * Currently, the only external dependency is MySQL, so the deployment is very simple. Apollo can run as long as Java
      and MySQL are installed
    * Apollo also provides a packaging script, which can generate all required installation packages with just one
      click, and supports customization of runtime parameters

# Usage

1. [Apollo User Guide](https://www.apolloconfig.com/#/zh/usage/apollo-user-guide)
2. [Java SDK User Guide](https://www.apolloconfig.com/#/zh/usage/java-sdk-user-guide)
3. [.Net SDK user Guide](https://www.apolloconfig.com/#/zh/usage/dotnet-sdk-user-guide)
4. [Third Party SDK User Guide](https://www.apolloconfig.com/#/zh/usage/third-party-sdks-user-guide)
5. [Other Language Client User Guide](https://www.apolloconfig.com/#/zh/usage/other-language-client-user-guide)
6. [Apollo Open APIs](https://www.apolloconfig.com/#/zh/usage/apollo-open-api-platform)
7. [Apollo Use Cases](https://github.com/apolloconfig/apollo-use-cases)
8. [Apollo User Practices](https://www.apolloconfig.com/#/zh/usage/apollo-user-practices)
9. [Apollo Security Best Practices](https://www.apolloconfig.com/#/zh/usage/apollo-user-guide?id=_71-%e5%ae%89%e5%85%a8%e7%9b%b8%e5%85%b3)

# Design

* [Apollo Design](https://www.apolloconfig.com/#/zh/design/apollo-design)
* [Apollo Core Concept - Namespace](https://www.apolloconfig.com/#/zh/design/apollo-core-concept-namespace)
* [Apollo Architecture Analysis](https://mp.weixin.qq.com/s/-hUaQPzfsl9Lm3IqQW3VDQ)
* [Apollo Source Code Explanation](http://www.iocoder.cn/categories/Apollo/)

# Development

* [Apollo Development Guide](https://www.apolloconfig.com/#/zh/development/apollo-development-guide)
* Code Styles
    * [Eclipse Code Style](https://github.com/apolloconfig/apollo/blob/master/apollo-buildtools/style/eclipse-java-google-style.xml)
    * [Intellij Code Style](https://github.com/apolloconfig/apollo/blob/master/apollo-buildtools/style/intellij-java-google-style.xml)

# Deployment

* [Quick Start](https://www.apolloconfig.com/#/zh/deployment/quick-start)
* [Distributed Deployment Guide](https://www.apolloconfig.com/#/zh/deployment/distributed-deployment-guide)

# Release Notes

* [Releases](https://github.com/apolloconfig/apollo/releases)

# FAQ

* [FAQ](https://www.apolloconfig.com/#/zh/faq/faq)
* [Common Issues in Deployment & Development Phase](https://www.apolloconfig.com/#/zh/faq/common-issues-in-deployment-and-development-phase)

# Presentation

* [Design and Implementation Details of Apollo](http://www.itdks.com/dakalive/detail/3420)
    * [Slides](https://github.com/apolloconfig/apollo-community/blob/master/slides/design-and-implementation-of-apollo.pdf)
* [Configuration Center Makes Microservices Smart](https://2018.qconshanghai.com/presentation/799)
    * [Slides](https://github.com/apolloconfig/apollo-community/blob/master/slides/configuration-center-makes-microservices-smart.pdf)

# Publication

* [Design and Implementation Details of Apollo](https://www.infoq.cn/article/open-source-configuration-center-apollo)
* [Configuration Center Makes Microservices Smart](https://mp.weixin.qq.com/s/iDmYJre_ULEIxuliu1EbIQ)

# Community

* [Apollo Team](https://www.apolloconfig.com/#/en/community/team)
* [Community Governance](https://github.com/apolloconfig/apollo/blob/master/GOVERNANCE.md)
* [Contributing Guide](https://github.com/apolloconfig/apollo/blob/master/CONTRIBUTING.md)

# License

The project is licensed under the [Apache 2 license](https://github.com/apolloconfig/apollo/blob/master/LICENSE).


# Awards

<img src="https://cdn.jsdelivr.net/gh/apolloconfig/apollo-community@master/images/awards/oschina-2018-award.jpg" width="240px" alt="The most popular Chinese open source software in 2018">

# Stargazers over time

[![Stargazers over time](https://api.star-history.com/svg?repos=apolloconfig/apollo&type=Date)](https://star-history.com/#apolloconfig/apollo&Date)
