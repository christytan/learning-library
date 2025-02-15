---
layout: ziplab
description: Learn how to launch a Virual Machine using Oracle Cloud Infrastructure Computer Service
tags: Oracle Cloud, Oracle Cloud Infrastructure, OCI, Virtual Machine, VM, Virtual Cloud Network, VCN
permalink: /ziplabs/test/index.html
---

# Lab 2: Deploying an Autonomous Exadata Infrastructure in a private OCI network #

## Introduction ##
An Autonomous Exadata Infrastructure (AEI) resource allocates an available Oracle Exadata Database Machine to you. Its primary purpose is to act as a bridge between the hardware and software components of your dedicated infrastructure. You must create at least one Autonomous Exadata Infrastructure resource before you can create any of the other kinds of dedicated infrastructure resources such as Autonomous Container Databases or simply an Autonomous Database instance.

To **log issues**, click [here](https://github.com/oracle/learning-library/issues/new) to go to the github oracle repository issue submission form.

### Objectives ###

As a fleet administrator, 
- deploy an Autonomous Exadata Infrastructure in a pre-provisioned private network in your OCI account
- Understand AEI maintenance scheduling
- Understand database licensing options

### Required Artifacts ###
- An Oracle Cloud Infrastructure account with service limits to deploy at least one 1/4 rack of Exadata Infrastructure in any one region or Availability Domain.
- You also need privileges to create Autonomous Exadata Infrastructure and a container database in a pre-provisioned compartment and network.




## Deploy your Autonomous Exadata Infrastructure (AEI) ##

### LOGIN ###

- Login to your OCI account as a fleet administrator 

Navigate to the 'Autonomous Transaction Processing' option in the top left hamburger menu from your OCI home screen

![create_aei1](./img/create_aei1.png)


### Autonomous Exadata Infrastructure ###

- Select 'Autonomous Exadata Infrastructure' and ensure you pick the fleet compartment as shown above. Click the blue 'Create Autonomous Exadata Infrastructure' button 



![create_aei3](./img/create_aei3.png)

### Network Configuration ###

- In the network section, select,
    - The compartment that hosts the VCN; typically the fleetCompartment
    - Name of the VCN
    - The compartment that hosts the subnet, also fleetCompartment
    - The subnet to hold the exadata infrastucture

Your network or fleet administrator needs to setup the network before you can deploy an AEI. Please contact your network / account admin if a suitable network is not visible in the drop down options

You can also modify the exadata and database maintenance schedules at this time. Click the 'Modify Schedule' button and specify the quarter, week, day and time you would like to schedule automatic maintenance for your exadata hardware and container databases

![select_schedule](./img/select_schedule.png)

You also have two options for selecting the license type for the database containers (ACDs) you deploy on your autonomous exadata infrastructure. You can either bring your spare corporate database licenses to OCI or you can buy a license subscription in the cloud. Pick the best option for you and hit the Create button. Your AEI will soon be ready to deploy autonomous container databases.

![license_type](./img/license_type.png)


All Done! You have successfully deployed your Autonomous Exadata Infrastructure and it should be available shortly.
