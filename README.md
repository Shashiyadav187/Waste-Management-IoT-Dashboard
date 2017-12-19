# Waste Management IoT Dashboard

This is a simple Node.js azure website that shows how to visualize data from eventhub as a real-time graph using D3.js.

## Acknowledgements

This code was modified from the sample [ThingLabs-IoT-Dashboard](https://github.com/irjudson/ThingLabs-IoT-Dashboard).

## Installing to Azure Web App with FTP

1. From the Azure Portal, using the "Node JS Empty Web App" Template create a Node.js Web App 
2. From Web App -> Properties copy the ftp user and ftps url
2. From Web App - > Application Settings
    | key | Value |
    |---|---|
    | WEBSITE_NODE_DEFAULT_VERSION |8.9.3 |
    | EVENTHUB_CONNSTRING | Event Hub Connection String for sensor data  |
    | EVENTHUBNAME | defaults to 'charts'|
    | SENSOR_STATE_TABLE_CONNSTRING | SensorState Table Storage connection string |

3.  From Appliction Settings turn on **Web sockets**

3.  Create Deployment Creditials
    * Azure Portal -> Your Web App -> Deployment Creditials


4. Using your faviourite FTP program (eg FileZilla), copy application including package.json, and web.config. Do not the node_modues directory or the package-lock.json file
5. Install NPM Modules into the Web App
    * Azure Portal -> Web App -> Advanced Tools -> Go -> Debug Console -> CMD
    * cd sites/wwwroot
    * run 'npm install'. This will install packages listed in the package.json file
6.  Dianostics
    * Web App -> Diagnostics, enable Application Logging
    * Web App -> Live Stream to review issues



