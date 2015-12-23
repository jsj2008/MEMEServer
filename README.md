# JINS MEME iOS API Server


## Installation

[1] Download this project

```
$ git clone https://github.com/InolabSF/MEMEServer.git
$ cd MEMEServer
```

[2] Install [CocoaPods](https://guides.cocoapods.org/using/getting-started.html)

[3] Input the command

```
$ pod update
```

[4] Registration

[Register your account](https://developers.jins.com/en/preregistration/)

[Create an App](https://developers.jins.com/en/apps/create/)

[5] Open workspace

```
$ open MEME.xcworkspace
```

[6] Run codes


## Server

IP Address: your iPhone's IP Address

Port: 3000

### MEMELib

It's implemented by HTTP Server.

```
API: /isConnected
responseBody: {"api":"isConnected", "return":BOOL}

API: /isDataReceiving
responseBody: {"api":"isDataReceiving", "return":BOOL}

API: /isCalibrated
responseBody: {"api":"isCalibrated", "return":BOOL}

API: /set?appClientId=YOUR_MEME_SDK_APP_CLIENT_ID&clientSecret=YOUR_MEME_SDK_CLIENT_SECRET
responseBody: {"api":"setAppClientId:clientSecret:", "return":"void"}

API: /startScanningPeripherals
responseBody: {"api":"startScanningPeripherals:", "return":MEMEStatus}

API: /connect?peripheral=YOUR_PERIPHERAL_UUID_STRING
responseBody: {"api":"connectPeripheral:", "return":MEMEStatus}

API: /disconnectPeripheral
responseBody: {"api":"disconnectPeripheral", "return":MEMEStatus}

API: /getConnectedByOthers
responseBody: {"api":"getConnectedByOthers", "return":PERIPHERALS_UUID_STRING_ARRAY}

API: /startDataReport
responseBody: {"api":"startDataReport", "return":MEMEStatus}

API: /stopDataReport
responseBody: {"api":"stopDataReport", "return":MEMEStatus}

API: /getSDKVersion
responseBody: {@"api":@"getSDKVersion", @"return":SDKVersion}

API: /getFWVersion
responseBody: {"api":"getFWVersion", "return":FWVersion}

API: /getHWVersion
responseBody: {"api":"getHWVersion", "return":HWVersion}

API: /getConnectedDeviceType
responseBody: {"api":"getConnectedDeviceType", "return":MEMEType}

API: /getConnectedDeviceSubType
responseBody: {"api":"getConnectedDeviceSubType", "return":MEMEType}
```
