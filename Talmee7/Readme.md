# Talmee7 Educational Platform
[Talmee7 Platform](https://talmee7.drolez-apps.cloud)

## Overview
`Talmee7` is an online platform fetches content from all Ncms Instances

## My Role
> 1. Software Architect
> 2. Team Lead

## Technologies & Specifications
1. `3-tier` architecture
2. `Arte PHP API`
3. `MySQL`
4. Secure Communication to all Ncms Instances
4. `AWS S3 Buckets` to host huge session files
5. `REST API`
6. UI built in `components` structure for reusability & organization
7. `Bootstrap` & `jQuery` UI
8. Documented on `Postman`

## Features
### Managerial Aspects
1. Students register and apply to join learning groups
2. Admins Review and Approve/reject the student or recommends other groups for him
3. Subscription fees are automatically calculated and notifies both admins and users about due dates.
4. Statistical Dashboard to view students' peroformance throughout the year

### Online Content
1. Admin can organize his content in the form of courses
2. Courses are protected with `access codes`
3. Online sessions can include `exams` and `homeworks` with due dates
4. The admin can construct his question bank that he can then use to build exams and homeworks
5. Automated Marking

### Society & Utilities
1. Chat System
2. Posts & Announcements
3. Calendar for every user reminds him of his duties

## Back-end (Technical Keypoints)
1. SAAS nature allows instantiating separated instances for every client with dedicated database and FHS
2. S3 buckets allows hosting terabytes of content without worrying about performance, access time, or memory usage
3. Generating stats for students at the moment the exam ends was too slow especially that many students access exam results at the same time putting too much load on the server. So I adjusted Arte to be able to close the TCP connection, outputs the response buffer, and continue processing to provide the client with immediate response and informs him about `still processing` status. That was the first brick into building Arte powerful background processes wrappers.