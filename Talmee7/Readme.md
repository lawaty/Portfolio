# Talmee7 Educational Platform
[Talmee7 Platform](https://talmee7.drolez-apps.cloud)

## Overview
`Talmee7` is an online platform fetches content from all Ncms Instances and packages them in groups of teachers, chapters, etc... This helps `create packaged contents` and make better offers for students.

## My Role
> 1. Software Architect
> 2. Team Lead

## Technologies & Specifications
1. `3-tier` architecture
2. `Arte PHP API`
3. `MySQL`
4. `Secure Tunnel` communication to all Ncms Instances
6. `NextJS`
7. `Flutter` Mobile App
8. `Python Automation`


## Features
### Talmee7 Admin Dashboard
1. Links Ncms instances with talmee7
2. Displays/Manages all linked instances' content to be structured and featured on talmee7
3. Admin can create packages, add content to it from linked instances, and manage all other information like subscription fees, etc...
4. Python Automation Script automates content upload, package creation, and others. This script can be run on multiple servers and all of them are trackable from the dashboard

### Front Views
1. Smart Wallet
2. Session Content Views
3. Exams and Homeworks
4. Student Stats

## Back-end (Technical Keypoints)
1. After releasing Talmee7, many teachers joined the platform and content size spiked to more than 100 GB in special weeks. As a result, we implemented a `python automation script` that allows uploading files `24/7 on multiple servers` (typically 3 servers). The script was greatly error-tolerant that even under poor internet conditions, it was able to finish the upload in a reasonable time. It also provided trackers with great feedback so that we can track it over from anywhere.
2. Connecting Talmee7 to all Ncms Instances required designing a `one-way authorization in Ncms` allows only Talmee7 server to access their data. Even Talmee7 wasn't able to access teacher's protected content that he selects by himself.
3. The biggest challenge we faced is that we built this platform in a single month work.