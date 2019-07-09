# Virtual N Way Switch app for Hubitat
Virtual N Way Switch is a an app to make a 3 or 4 way switch in Hubitat. it solves the continous on/off cycle created by Hubitat's broken Z-wave radio. 
## Purpose

Virtual N Way Switch is a project to make a 3 or 4 way switch group. It replaces Simple app in one very important way. It is written to reduce events and is written to ensure that you do not get cascading on/off effect where your lights are turning off and on constantly. This is an issue I’ve had with the Simple Application and Rule Machine. The real issue here if Hubitat’s Z-wave radio being extremely broken. If you have more than a few devices communicate at the same time on a Hubitat z-wave network everything screeches to a halt and events get delayed by up to minutes. So you can have an on and an off event that are delayed enough to trigger a second round of a rule or simple Lighting again. This makes more events that are still delayed that will trigger those again. This solves that buy making a configurable sliding timeout that makes the first device to report an event the “owner” of the group until the app no longer is getting events trying to trigger it. And only the “Owner” can trigger a change again. This allows for a user to change their mind but blocks out all those events made by the other devices in the group. 

## Installation

Step 1:
Install Nway.groovy and NwayInstance.groovy as user Apps in Hubitat 
Step 2: 
install "Virtual 3-way Switch" under Apps
Step 3: 
use the app to create the Nway groups that will turn off and on together. 
Step 4:
Profit!
 


# CHANGES

