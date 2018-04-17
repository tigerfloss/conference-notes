# Understanding How to Implement Alexa Home Automation Skills
Speaker: Jeremy Proffitt

### What are Hpme Automation SKills?
Unlike a custom skill, home automation skills have a standard command structure designed to operate items in the home like lights, power outlers, locks and thermostats. Recently, Version 3 added multimedia controls, including channels, volume, media and input controls

Examples:
- Alexa, Fireplace off
- Alexa, make living room blue
- Alexa, lock front door
- Alexa, what is the temperature of my house?


### What is require to build an Home Automation Skill?
* AWS Skill Linking to:
  * AWS Lambda written in Python, Node.JS, C#, or Java
  * oAuth user access management supporting access tokens
* Something to control "the something"
* Cloud based transport later to bridge the Lambda wit hthe something
Note: All communication to and from the Lambda function are in JSON

#### Account Linking - oAuth Access Token Requirements
In order to identify which devices belong to you, Home Automation SKills require you to link your Amazon Alexa account with your specific device cloud using oAuth Access Token

## The Flow for Device Discovery
1. The user invokes Discover Devices
2. Lambda is sent Deiscover Devices Request w/ oAuth
3. Lambda retrieves a list of physical devices from the Particle.IO cloud
2. Lambda checks al physicla devices

## The Flow for Device Usage
1. User Command
2. oAtuh, automationa device identifier
3. Lambda calls Particle.IO
4. Particle.IO cloud contacts the physical device sendin it the command and returning any requested information
5. The particle.IO cloud returns the information to the lambda
6. The lambda returns the information to the Echo System
7. The Echo either respons "OK" or provides the requested information

## The donwfall of a Lambda Based System
- You are lock into paying Amazon for every time a customer uses their device, this means building in the application cost into the initial device price or moving to a subsciption based plan
- Amazon charges bu the 100ms for lambda usage, so the longer your code, and the communication with tour devices take, the more it will cost.-
- Communcation timeout with the world outside your Lambda need to be short
 - If the Lambda times out while doing a device discovery, no devices will be discovered
 - If the Lambda times out while communcating with your device, the device may not get the command, or the user may have a bad user expericence of the device

## Introduction to the Particle.IO photon
### Particle.IO IDE

## Q&A
### Does the lambda cost money?
> Yes. Lambda costs money relative to storage, volume usage, how many times ran

### How do you promote the skils that you developed?
> They're trying to make Alexa accessible to the public. Increasing user volume. Promotion at the alexa appstore. They're not really there to promote your skill 

### What type of skills are mostly used?
> Games! 


