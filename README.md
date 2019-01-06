---
title: JBDevice
description: Get device information.
---

基于cordova-plugin-device 2.0.3-dev版本修改

# cordova-plugin-jb-device

This plugin defines a global `device` object, which describes the device's hardware and software.
Although the object is in the global scope, it is not available until after the `deviceready` event.

```js
document.addEventListener("deviceready", onDeviceReady, false);
function onDeviceReady() {
    console.log(device.cordova);
}
```

## Installation

    cordova plugin add cordova-plugin-jb-device

## Properties

- cordova
- model
- platform
- uniqueid
- version
- manufacturer
- isVirtual
- idfa

cordova.plugins.JBDevice.getInfo(function(info){
              var html = "<br/> 设备上的cordova版本：" + info.cordova +
               "<br/> 设备名称：" + info.model +
               "<br/> 设备平台系统：" + info.platform +
               "<br/> 设备唯一标识符" + info.uniqueid +
               "<br/> 设备平台操作系统版本号：" + info.version +
               "<br/> 设备平台制造商：" + info.manufacturer+"<br/> idfa：" + info.idfa ;

                 alert(html);
            },function(error){


            });

