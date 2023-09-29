# Qualification Test Procedure

## 1. Introduction

This document outlines the qualification test procedure for an advanced aeronautical tablet interface (referred to as the DUT). The purpose of this procedure is to subject the DUT to a series of environmental tests designed to assess its ability to function under various conditions. Please refer to the image below for a visual representation of the DUT.

![QTP DUT](qtp-dut.png)

### Reference Documents

The following documents are referred to in this procedure:

- ASTM E171/E171M-18, Standard Practice for Conditioning and Testing Flexible Barrier Packaging
- RTCA DO-160, Environmental Conditions and Test Procedures for Airborne Equipment

### Safety Warnings and Notes

Safety must be the primary concern when conducting these tests. Always follow proper safety procedures and use appropriate personal protective equipment (PPE).

- Always handle the environmental chamber's controls with clean hands.
- Avoid touching the interior surfaces of the chamber as this can affect the temperature and humidity readings.
- Handle the DUT with care to avoid dropping or causing mechanical damage.

## 2. Pre-Test Verification

Before starting the environmental tests, perform an initial check of the DUT's functionality. Make sure the DUT is functioning as expected and all features are working. Enable the screen test pattern on the DUT for visual monitoring during the tests. Record the initial state of the DUT, including photographs if possible.

## 3. Test Setup

### Physical Setup of the DUT

Place the DUT in the center of the environmental chamber. Ensure that the DUT is positioned in such a way that it allows for even airflow around it. This will help maintain consistent temperature and humidity conditions around the DUT during the test.

To ensure a uniform temperature distribution around the DUT, consider placing the DUT on a rack or stand made of a thermally non-conductive material like Teflon or plastic. This will prevent direct contact between the DUT and the metal surfaces of the chamber which could lead to uneven heating or cooling.

### Loading the Environmental Test Profile

Load the pre-set environmental profile into the chamber's control system. This profile is designed to execute the high-temperature, high humidity, and low-temperature tests consecutively. Each stage is set to adjust the chamber conditions accordingly and maintain them for the specified duration.

## 4. Test Procedure

!!! Info "If a failure occurs during any stage of the test, the test can be restarted from that stage after addressing the cause of the failure."

1. **Start the Test:** Start the execution of the environmental profile. The chamber's control system or connected software will monitor the progress of the test.

2. **Monitor the DUT:** Monitor the functionality of the DUT throughout the test. Record any changes in performance or any failures that occur.

3. **Report Upload:** At the end of each stage of the test, upload the environmental chamber's temperature and humidity data and your observations of the DUT's performance to the designated data management system.

| Test Stage | Chamber Condition | Duration | Description |
|------------|-------------------|----------|-------------|
| High-Temperature | 55°C (maximum operating temperature) | 4 hours | Monitor device functionality, temperature, and time |
| High Humidity | 95% RH at 40°C | 4 hours | Monitor device functionality, humidity, temperature, and time |
| Low-Temperature | -20°C (minimum operating temperature) | 4 hours | Monitor device functionality, temperature, and time |

## 5. Post-Test Verification

### Returning the Chamber to Normal Conditions

After the completion of the environmental test, the chamber conditions need to be returned to their normal state. Follow these steps:

1. **Stop the Test:** Stop the environmental profile on the chamber's control system.

2. **Normalize the Chamber Conditions:** Set the temperature and humidity controls to return the chamber to room conditions (approximately 23°C and 50% RH). Allow the chamber to stabilize for at least 1 hour.

3. **Power Off the Chamber:** Once the chamber has returned to normal conditions and the DUT has been removed, turn off the environmental chamber.

!!! warning "Always ensure the chamber has returned to safe conditions before opening and handling the DUT."

### Removal of the DUT

Carefully remove the DUT from the chamber. Handle the DUT with care to prevent any mechanical damage. Place the DUT on a clean, stable surface for the post-test inspection.

### Post-Test Inspection

Perform a detailed inspection of the DUT after it has been removed from the chamber and has returned to room temperature. Follow these steps:

1. **Visual Inspection:** Check for any visible signs of damage or degradation. This includes discoloration, warping, melting, cracking, or any other physical damage.

2. **Power Up:** Power up the DUT to verify it can be turned on after the environmental tests.

3. **Functional Tests:** Test the functionality of the DUT, including screen display, touch screen, buttons, ports, speakers, and any other features. Record any changes in performance or any failures.

4. **Final State Record:** Record the final state of the DUT, including photographs if possible. Upload these records to the designated data management system.

**Table 5.1: Post-Test Inspection Checklist**

| Inspection Item   | Pass | Fail |
|-------------------|------|------|
| Visual Damage     | [✔](#) | [✖](#) |
| Power Up          | [✔](#) | [✖](#) |
| Functional Tests  | [✔](#) | [✖](#) |
