# Web BLE App Documentation

## Introduction

This document provides an overview and documentation for the JavaScript code used in a web application to interact with a BLE device (e.g., ESP32) using the Web Bluetooth API. The application allows connecting to a BLE device, reading and writing characteristics, and handling disconnections.

## Table of Contents

1. [Getting Started](#getting-started)
2. [BLE Device Specifications](#ble-device-specifications)
3. [Global Variables](#global-variables)
4. [Event Listeners](#event-listeners)
5. [Functions](#functions)
6. [Utility Functions](#utility-functions)
7. [Conclusion](#conclusion)

## 1. Getting Started

Ensure that the web browser supports the Web Bluetooth API. The application is designed to connect to a BLE device (e.g., ESP32) with specific characteristics.

## 2. BLE Device Specifications

Define the specifications of the target BLE device:

- **Device Name:** ESP32
- **BLE Service UUID:** 19b10000-e8f2-537e-4f6c-d104768a1214
- **LED Characteristic UUID:** 19b10002-e8f2-537e-4f6c-d104768a1214
- **Sensor Characteristic UUID:** 19b10001-e8f2-537e-4f6c-d104768a1214

## 3. Global Variables

- `bleServer`: Represents the GATT server after connecting to the BLE device.
- `bleServiceFound`: Represents the discovered BLE service.
- `sensorCharacteristicFound`: Represents the discovered sensor characteristic.

## 4. Event Listeners

- `connectButton`: Event listener for the "Connect" button.
- `disconnectButton`: Event listener for the "Disconnect" button.
- `onButton`: Event listener for the "ON" button.
- `offButton`: Event listener for the "OFF" button.

## 5. Functions

- `isWebBluetoothEnabled()`: Checks if the Web Bluetooth API is supported in the browser.
- `connectToDevice()`: Initiates the connection to the BLE device and sets up notifications.
- `onDisconnected(event)`: Handles the disconnection event and attempts to reconnect.
- `handleCharacteristicChange(event)`: Handles changes in the characteristic value and updates the UI.
- `writeOnCharacteristic(value)`: Writes a value to the LED characteristic.
- `disconnectDevice()`: Disconnects from the BLE device and stops notifications.
- `getDateTime()`: Returns the current date and time in a formatted string.

## 6. Utility Functions

- None

## 7. Conclusion

This Web BLE application provides a basic framework for connecting to a BLE device and interacting with its characteristics. Further customization can be done based on specific project requirements.
