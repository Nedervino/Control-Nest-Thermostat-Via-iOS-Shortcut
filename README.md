# iOS Shortcut for Controlling Nest Thermostat

This repository contains an iOS Shortcut that allows you to automatically adjust the temperature of your Nest thermostat to a specified temperature, and is compatible with any generation of Nest Thermostat (without requiring a separate hub or Matter support). It enables Nest automations not currently supported via Apple's current Home automation, such as turning off your Nest Thermostat whenever you leave the house.

Given [all Nest thermostats except for the 2020 model are incompatible with Apple's Home automation suite / Homekit](https://9to5google.com/2023/05/11/nest-thermostat-homekit-matter-set-up/), this iOS shortcut uses a workaround by directly interacting with Google's Device Access API for Nest. As this API is secured using OAuth2, you will first need to register for Google Nest developer access and go through a few developer-oriented steps before the Shortcut can be used. 

## Example flow enabled by the shortcut
![Nest Thermostat Control Screenshot](./screenshots/turn-down-thermostat-when-leaving-home-shortcut.png)

## Prerequisites

1. **Register your account and Nest device for Nest's Device Access API**
Complete the first two steps (Get Started and Authorize an Account) described in the [Google Nest Device Access documentation](https://developers.google.com/nest/device-access/get-started). Make sure to complete all steps up to and including "How to use a refresh token. While walking through these steps, make sure to note down the following variables which you will need to populate in the Shortcut before you can trigger it. Make sure you note down the following values:
- Client ID
- Client secret
- Refresh token
- Project ID 
- Device ID (for your already installed Nest thermostat)
    - This can be retrieved from the response for the request performed in the [Make a device list call](https://developers.google.com/nest/device-access/authorize#make_a_device_list_call) step

2. **Install the shortcut on your iPhone**
Installing the shortcut on your iPhone can either be achieved by downloading the shortcut file from this repository and opening it on your iPhone, or through the following link: https://www.icloud.com/shortcuts/b62f4f9adbec47c8b14d2dda57db094b

3. **Populate the Dictionary**: When clicking on the iOS Shortcut, you'll see a Dictionary with a few placeholders for custom values (e.g. Client Secret, Client ID) at the top of the shortcut flow. You need to fill in the ‘Value’ fields of the Dictionary with the variables you gathered from the previous step. Replace the placeholders (e.g. <YOUR_CLIENT_ID>) with your actual values

4. (Optional) define a custom trigger event, such as leaving your home, when the shortcut should be triggered

## How it works
![Nest Thermostat Control Screenshot](./screenshots/nest-thermostat-control-ios-shortcut.png)

