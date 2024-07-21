# Arte Framework
[Documentation](https://github.com/lawaty/Arte-Documentation)

## Overview
Arte was created to address the common challenges faced by developers when managing database interactions and API endpoints. Its primary goal is to enhance productivity by automating repetitive tasks and offering a modular, flexible architecture.

## My Role
> 1. Software Architect
> 2. PHP Developer

## Technologies & Specifications
1. Native PHP
2. SqLite & MySQL
3. Architectural and Design Patterns
4. OTA System Upgrade
5. JWT Token Authorization

## Features
1. **Performance and Organization**: Arte emphasizes performance and organizational efficiency, ensuring that developers can build robust applications with minimal overhead. The framework's design allows for the seamless integration of essential functionalities while maintaining optimal performance.

2. **Modular Architecture**: The framework's architecture is split into two primary sections:
    - **Arte Core**: Contains framework-related components, base classes, and utilities for handling repetitive tasks.
    - **Arte App**: Developers define application-specific elements, organized into:
        - **Model Layer**: Manages system logical entities, database mappers, and services.
        - **Endpoints Layer**: Implements logical endpoints that utilize entities and services to deliver output.

3. **Straightforward and automated `persistance-to-logic` mapping**:
Arte's framework leverages the `Entity` and `Mapper` classes to provide a structured approach to data management and interaction. The `Entity` class represents system entities, while the `Mapper` class handles data persistence and retrieval, ensuring a clean and maintainable codebase.

4. **Automated Repetitive Tasks**: Arte automates various repetitive development tasks, including database operations, data validation, and entity management, allowing developers to focus on core functionalities.

5. **Flexibility and Extensibility**: Arte is designed with flexibility and extensibility in mind, allowing developers to easily extend the framework's core functionalities to meet specific requirements.

6. **Performance Optimization**: Arte includes built-in performance optimizations, such as efficient database querying and caching mechanisms, to ensure high performance even under heavy loads.

7. **Security**: Arte incorporates robust security features, including input sanitization, protection against SQL injection, and secure authentication methods, to safeguard applications.

8. **OTA update**: for licensed copies.


## Back-end (Technical Keypoints)
1. `Validator` Service can validate massively huge and complex data schemas using nested validator instantiation and customizable validation callbacks.
2. Making use of the Entity-Mapper combination properly can automate all persistence layer interactions and let you focus on higher level logic
3. `CustomMapper` class and `db-script` are two utilities in the system that can ***automatically*** generate even `join queries` for you without writing a single SQL statement saving lots of hassle from you
4. `Entity`-`Mapper` combination provides `memoization` and `Lazy-Loading` to enhance and reduce intensive operations.  
5. `Arte Automation` generate a join schema that can join mappers together without writing sql queries at all using `CustomMapper->join(mapper1, mapper2, mapper3)`
6. `Arte Endpoint` base allows automating tests following `AAA` testing pattern
7. `Arte Store` allows licensed users to publish/install plugins in a handy manner
8. Arte Base support `OTA update` for licensed users


## Projects built with Arte

Proudly, Arte has been used to build over 30 web apps so far including the following:
- Ncms SAAS Instances
- [Mynty Collections](https://mynty.gg): integrated with an existing wordpress system
- [Auto Trader](https://auto-trader.drolez-apps.cloud): Have a look at Auto-Trade/Readme.md
- [HpEMR](https://stg.hpemr.ca): integrated with an existing Symphony system
- HpEMR Dashboard API: built completely with Arte with Arte aws plugin to communicate with aws lambda and dynamo db.
- [Talmee7](https://talmee7.drolez-apps.cloud)
- [Ndo](https://ndo.drolez-apps.cloud)
- [Ip Geeks API](https://messages-dev.conversational.net)
- [El Avocato API](https://el-avocato.live)