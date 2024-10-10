# iOS Shortcut for Controlling Nest Thermostat

This repository contains an iOS Shortcut that allows you to adjust the temperature of your Nest thermostat to a specified temperature, and is compatible with any generation of Nest Thermostat. You can e.g. use it to automatically turn off your Nest Thermostat when leaving the house. 

Given [all Nest thermostats except for the 2020 model are incompatible with Apple's Home automation suite / Homekit](https://9to5google.com/2023/05/11/nest-thermostat-homekit-matter-set-up/), this iOS shortcut uses a workaround by directly interacting with Google's Device Access API for Nest. As this API is secured using OAuth2, you will first need to register for a Google Nest developer account and go through a few developer-oriented steps before the Shortcut can be used. 

## Example flow
![Nest Thermostat Control Screenshot](./screenshots/turn-down-thermostat-when-leaving-home-shortcut.png)

## Prerequisites

1. **Register your account and Nest device for Nest's Device Access API**
Walk through the first two steps (Get Started and Authorize an Account) described in the [Google Nest Device Access documentation](https://developers.google.com/nest/device-access/get-started). Make sure to complete everything up to and including "How to use a refresh token. During the setup process, you'll need to collect certain values that you need to populate in the Shortcut before you can trigger it. Make sure you note down the following values while walking through the steps:
- Your client ID.
- Your client secret.
- Your refresh token.
- Your access token.
- Your Nest device ID.

2. **Install the shortcut on your iPhone**
Download the shortcut from this repository and open it on your iPhone, or access it using the following link: TODO

3. **Populate the Dictionary**: When clicking on the iOS Shortcut, you'll see a Dictionary with a few placeholders for custom values (e.g. Client Secret, Client ID) at the top of the shortcut flow. You need to fill in the ‘Value’ fields of the Dictionary with the variables you gathered from the previous step. Replace the placeholders (e.g. <YOUR_CLIENT_ID>) with your actual values

4. (Optional) define a custom trigger event, such as leaving your home, when the shortcut should be triggered

## How it works
![Nest Thermostat Control Screenshot](./screenshots/nest-thermostat-control-ios-shortcut.png)

