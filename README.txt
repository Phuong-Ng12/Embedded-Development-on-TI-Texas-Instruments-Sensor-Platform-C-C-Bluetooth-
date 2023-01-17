Embedded Development on TI (Texas Instruments) Sensor Platform project.
This project aims to optimize power life of battery life on TI SensorTag CC2650STK by reducing the 
advertising interval of the sensor through bluetooth. 

To test the code, please follow these steps: 

Step 1: Download Code Composer Studio (CCS)
- Visit https://www.ti.com/tool/CCSTUDIO and select suitable download options to your computer

Step 2: Download BLE-STACK-ARCHIVE
- Visit https://www.ti.com/tool/BLE-STACK-ARCHIVE and select BLE-STACK-2-2-2

Step 3: Load code in project zip files as CCS project
3.1. Unzip the project zip files at C:\ti\simplelink\ble_sdk_2_02_02_25\examples (assume that you downloaded BLE-STACK-ARCHIVE at C:\)
3.2. Open CCS. Select Project -> Import CCS Projects... -> Browse to the directory in step 3.1
3.3. Click Select Folder -> Finish. Now the code in zip file is loaded in CCS.

Step 4: Build project in CCS
4.1. In Project Explorer, double click on sensortag_cc2650stk_app. Now it will show as "[Active - FlashOnly_OAD]"
4.2. Click Build hammer icon on the toolbar. This will take a while to finish building.
4.3. Do the same for sensortag_cc2650stk_stack. Both app and stack folder will be built successfully when no errors show.
If there are errors, it usually we're missing some libraries. We can go to ti.com to look for the libraries that are missing and load into our project, then build again..

Step 5: Load the code to debug on the SensorTag
5.1. Connect the debugger to the SensorTag, then connect it to your PC.
5.2. In CCS, click on Debug icon. You'll see red LED light flashing when the code is loading to the debugger.
5.3. After the loading is finished, click Resume icon to run the SensorTag through the debugger.
5.4. Now the SensorTag will flash red LED lights multiple times, a long beep sound will beacon along side with the red LED lights. 
This tells the SensorTag is starting and running successfully.

Step 6: Test the reduction of advertising interval of the SensorTag's bluetooth:
6.1. Open the SensorTag app on your mobile device (This can be downloaded on Android and iOS app store). 
Make sure the mobile device is in the same wifi network with the SensorTag, as well as bluetooth is on. 
6.2. Refresh the "BLUETOOTH LOW ENERGY DEVICES" section multiple times to see the SensorTag is not 
being discoverable all the time. Now the SensorTag will be discoverable in every 10000ms (10s), not at default 100ms. 

(Last edit made on Nov 30, 2022)


