# hubitat-govee-led-lights
Govee LED Light Strips integration for Hubitat Elevation

## UPDATED AS OF 2022-10-04
Govee has began limiteding the number of API calls an account is allotted to have. This happened back in May 2022, however it is being fully implemented now and is affecting users with multiple Govee devices accessing the API.
So this release (v2) updates with a parameter setting that allows the user to set their own "polling" time (in seconds).

### Pre-requisites
Must have a Hubitat Elevation Hub
Govee LED Light Strips
Govee API Key (generated from the Govee mobile app)

### To integrate this into Hubitat, you'll follow these steps:
To properly integration into Hubitat Elevation, please go to the following URL: https://www.deanberman.com/govee/hubitat/
This page will provide you step-by-step procedures on add the device and device type handlers into your SmartThings account.  You provide it your Govee API Key and it will retrieve the list of device ids, names, and models for the device preferences.

If you are more comfortable running the file(s) locally and have a webservice and php enabled locally, then you may download the index.html and the \_devices.php file and implement them locally (just update the index.html file for the URL reference location).

#### The following list of model numbers are currently supported (according to Govee API document):
Lights, Plugs, Switches:
H6160, H6163, H6104, H6109, H6110, H6117, H6159, H7022, H6086,
H6089, H6182, H6085, H7014, H5081, H6188, H6135, H6137, H6141,
H6142, H6195, H7005, H6083, H6002, H6003, H6148, H6052, H6143,
H6144, H6050, H6199, H6054, H5001, H6154, H6072, H6121, H611A,
H5080, H6062, H614C, H615A, H615B, H7020, H7021, H614D, H611Z,
H611B, H611C, H615C, H615D, H7006, H7007, H7008, H7012, H7013,
H7050, H6051, H6056, H6061, H6058, H6073, H6076, H619A, H619C,
H618A, H618C, H6008, H6071, H6075, H614A, H614B, H614E, H618E,
H619E, H605B, H6087, H6172, H619B, H619D, H619Z, H61A0, H7060,
H610A, H6059, H7028, H6198, H6049, H7031, H7032, H61A1, H61A2,
H61B2, H7061, H6067, H6066, H6009, H7041, H7042, H604A, H6173,
H615E, H604B, H6091, H7051, H7062, H618F, H605D, H6046, H601A,
H61A3, H610B, H6047, H7065, H61E1, H6057, H604C, H6065, H605C,
H705A, H705B, H7055, H61A5, H6078, H604D, H6168, H6601, H70B1,
H61A8

Appliances:
H7121, H7122, H7123, H7120, H7141, H7142, H7130, H7131, H7132,
H7150, H7160, H7101, H7111

### DEBUGGING/TROUBLESHOOTING
If you edit the driver code in your local Hubitat environment, search for the "refresh()" function and enable debugging by setting the following:  
```groovy
set_DEBUG("off")
...to...
set_DEBUG("on")
```

### DRIVER DISCLAIMER
After further testing, the API call for getting the device state may not work for all supported Govee models listed above.  Determing if it's a problem with the Govee API or if it's not supported due to the nature of the device model.

### DISCLOSURE
I am not a Hubitat developer, I just did this because I wanted to be able to integrate my multiple Govee LED Light strips into my Smart home network, so I created this myself.  It works well for me and this isn't for sale, so feel free to use it, tweak it, whatever you want!
Just a heads up, this isn't perfect by any means, so feel free to provide me some input and updates, I'll be happy to make them!

Your support will help further the development and integration of this driver code and other devices which may/may not be supported as of yet with Govee!

Enjoy!
