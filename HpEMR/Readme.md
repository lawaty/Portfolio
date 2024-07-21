# HpEMR

## Oveview
A clinic SAAS system built on top of the open source project `OpenEMR` which is a symphony-based web app. HpEMR implements the OntarioMD EMR Specifications. 

I was responsible for investigating OMD Specs and implementing them which is the `Export/Import` system in addition to building a super admin dashboard. `Export/Import` system is concerned with the operation of exporting and importing patients data from HpEMR while maintaining functional and non-functional requirement

## My Role
> 1. Software Architect
> 2. Full-Stack Developer

## Technologies:
1. [Arte PHP Framework](https://github.com/lawaty/Arte-Documentation)
2. Symphony
3. Arte Client front-end stack
4. aws lambda
5. Amazon Dynamo DB
6. XML Schema Validation

## Features
- Exporting specific patients by IDs
- Exporting specific information about the desired patients
- Exporting a certain physician’s patients
- Importing patients
- Linking patients to physicians
- Physicians CRUD (create, read, update and delete)
- Flexible, maintainable and `precise data validation base` that is modular and can be used for import/export or any other operation

## System Architecture
OpenEMR is still under development and evolves over time. We decided to separate our models and services completely from it so we used Arte API Framework to implement our system models. Arte API is a highly-flexible framework that allows overriding even core classes to better suit our needs

One important benefit from using Arte that is worth mentioning is that it allows `programmatic safe run` of all endpoints **without HTTP** Communication and this allowed running endpoints internally from openEMR interfaces without HTTP calls. Therefore, we can use OpenEMR existing authentication system and disable REST HTTP access.

Arte comes with a set of very useful set of tools like db migration utilities that provices `automated db migration` with a simple descriptive language.

## Technical keypoints
1. **Data Integrity**: The most crucial part of the system is data validation to protect our database from bad data and to ensure that all data entering and exiting HpEMR match the OntarioMD Specs. We started by Overriding Arte’s default validator to allow `nested structure validations` that it can now validate extremely complex and huge data structures (typically 3k+ XML Schema lines). [Learn more about Arte Validator](https://github.com/lawaty/Arte-Documentation)