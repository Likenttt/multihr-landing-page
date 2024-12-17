---
layout: page
title: Tutorial for Multi HR
include_in_header: true
---

## Introduction

Multi HR is an application designed for simultaneously monitoring and recording data from multiple Bluetooth heart rate devices. It features real-time data visualization, data export capabilities, and professional statistical analysis tools, making it particularly suitable for sports science research applications.

Disclaimer: This application is not intended for medical diagnosis but for digital evaluation and scientific research purposes only.

## Download

- [Multi HR iOS](https://apps.apple.com/us/app/multi-hr/id6739001386)
- [Multi HR Android](https://play.google.com/store/apps/details?id=com.niulasong.multihr)

## Key Features

- Simultaneous multi-device connection and monitoring
- Real-time heart rate data visualization
- Data recording and export (Excel/CSV)
- Professional statistical analysis (Pearson correlation coefficient, Bland-Altman analysis)
- Support for mainstream BLE heart rate devices with 0x180D service (Tested with Polar H10, Polar Sense, BigRun Team, HR01, Garmin 965 heart rate broadcast. Note: Apple Watch is not supported as it doesn't use the 0x180D service)

## User Guide

### Device Connection

- Launch the app and tap the search icon in the top right to scan for devices
- Locate your heart rate device in the available devices list
- Tap "Connect" to establish connection
- Connected devices will appear in the "Connected Devices" list

### Data Recording

- Tap the record button (red dot icon) in the top right to start recording
- View real-time heart rate graphs during recording
- Tap the record button again to stop recording
- Choose how to process the data:
  - Export as Excel
  - Export as CSV
  - Analyze data
  - Discard data

### Data Analysis

The app assumes you're using multiple heart rate devices, with one serving as a reference device and others as test devices. For example, using a Polar H10 as reference and an HR armband as test device.

The analysis page offers two main statistical methods:

#### Pearson Correlation Coefficient Analysis

- The Pearson correlation coefficient evaluates the linear correlation between two devices' measurements:
  - Range: -1 to 1
  - 1: Perfect positive correlation
  - -1: Perfect negative correlation
  - 0: No linear correlation
  - Interpretation standards:
    - |r| ≥ 0.8: Strong correlation
    - 0.5 �� |r| < 0.8: Moderate correlation
    - |r| < 0.5: Weak correlation

#### Bland-Altman Analysis

- Bland-Altman plots are essential tools for assessing agreement between two measurement methods:
  - X-axis: Mean of measurements from both methods
  - Y-axis: Difference between measurements
  - Center line: Mean difference
  - Upper/lower limits: 95% limits of agreement (±1.96SD)
  - Key interpretation points:
    - Random distribution of differences around zero
    - Presence of systematic bias (center line proximity to zero)
    - 95% of points within agreement limits
    - Relationship between differences and measurement magnitude

### Data Export

Two export formats are supported:

- Excel format (.xlsx)
  - Includes detailed timestamps
  - Multi-device data in separate columns
- CSV format
  - Universal format for easy import into other analysis software
  - Contains basic time and heart rate data

### Important Notes

- Before use, ensure:
  - Devices are fully charged
  - Bluetooth is enabled
  - Heart rate devices are properly worn
- During recording:
  - Keep devices within range
  - Maintain stable Bluetooth connection
  - Avoid backgrounding the app despite background permissions
- When analyzing data:
  - Ensure sufficient data quantity (recommend >5 minutes)
  - Identify outliers
  - Interpret results in context
