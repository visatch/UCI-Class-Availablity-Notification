# UCI Class Availablity Notification Service

The Python script continuously monitors the availability of a specified class every 30 minutes. If the class becomes available for enrollment or waitlisting, the script promptly notifies the user via email or SMS using a third-party service.

## Prerequisites

Before running this service, ensure you have Python installed on your system. This service is designed to run on any system with Python support, including Linux, macOS, and Windows, with a particular focus on server or Raspberry Pi setups for continuous operation.

## Required Packages

The service requires the following Python packages:

- `scheduler`: For scheduling tasks.
- `requests`: For making HTTP requests.
- `beautifulsoup4`: For parsing HTML and XML documents.
- `sinch`: For sending SMS or making voice calls as notifications.

## Installation

To install the required packages, run the following command:

```bash
pip install -r requirements.txt
```
## How to run it in the background

```bash
nohup python main.py & 
# It will output the process id back
```

## To ensure the script is working, you can perform of the two tests below
```
#First option
ps -aux | grep [m]ain.py # If it has a result, script is working normally.

#Second option
cat nohup.out #This file contains all the output from the main.py script, so if any error, it will show there.
```

