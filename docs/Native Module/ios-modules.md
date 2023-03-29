---
sidebar_position: 1
---

# iOS Modules

[Official Documentation](https://reactnative.dev/docs/native-modules-ios)

Steps:
  - Create Custom Native Module Header.
  - Create Corresponding Implementation file.
  - Export Module To JavaScript.
  - Test the Module from JavaScript.

## Create Header File

Add a new Objective-C file to the project that implements the `RCTBridgeModule` protocol

```ts MyModule.h
#import <React/RCTBridgeModule.h>

@interface MyModule : NSObject <RCTBridgeModule>

@end
```
## Create Module

```ts
#import "MyModule.h"

@implementation MyModule

// To export a module named MyModule
RCT_EXPORT_MODULE(MyModule);

RCT_EXPORT_METHOD(addNumbers:(int)number1
                  number2:(int)number2
                  resolver:(RCTPromiseResolveBlock)resolve
                  rejecter:(RCTPromiseRejectBlock)reject)
{
    int result = number1 + number2;
    resolve(@(result));
}

@end
```

### Create a JavaScript interface

```ts
import { NativeModules } from 'react-native';

const { MyModule } = NativeModules;

MyModule.addNumbers(2, 3, (result) => {
    console.log(result); // prints 5
});
```