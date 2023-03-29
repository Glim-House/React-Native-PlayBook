---
sidebar_position: 2
---

# Android Modules

[Official Documentation](https://reactnative.dev/docs/native-modules-android)

Some android related platform APIs are not available in the react-native itself. So, we have to create native modules. To create a new native module in android, must have a basic knowledge in java/kotlin and how to use android studio.

Steps to create android modules
  - Creating Native Module.
  - Exposing Native Module.
  - Registering the module.
  - Testing.

## Create the Module

Under `android/src/main/java/com/your-app-name/` Create an android module `MyModule.java` that extends `ReactContextBaseJavaModule`.

```ts title=MyModule.java
public class MyModule extends ReactContextBaseJavaModule {

    public MyModule(ReactApplicationContext reactContext) {
        super(reactContext);
    }

    @Override
    public String getName() {
        return "MyModule";
    }

    @ReactMethod
    public void addNumbers(int num1, int num2, Callback callback) {
        int result = num1 + num2;
        callback.invoke(result);
    }
}

```

### Create Packager

Create a new java file `CustomPackager.java` at your convenient path and extend it with `ReactPackage`

```ts title=MyModulePackage.java
public class MyModulePackage implements ReactPackage {

    @Override
    public List<NativeModule> createNativeModules(ReactApplicationContext reactContext) {
        List<NativeModule> modules = new ArrayList<>();

        // Add your custom native module class here
        modules.add(new MyModule(reactContext));

        return modules;
    }

    @Override
    public List<ViewManager> createViewManagers(ReactApplicationContext reactContext) {
        List<ViewManager> managers = new ArrayList<>();

        // Add your custom view manager class here
        // managers.add(new MyViewManager());

        return managers;
    }
}

```

### Register Package
Add the ReactPackage to your app's package list
In your app's `MainApplication.java` file, import your ReactPackage class and add an instance of it to the `getPackages()` method.

```ts title=MainApplication.java
import com.yourpackagename.MyModulePackage;

public class MainApplication extends Application implements ReactApplication {

  // ...

  @Override
  protected List<ReactPackage> getPackages() {
    return Arrays.asList(
        new MainReactPackage(),
        new MyModulePackage() // Add your package here
    );
  }
}

```

### Create a JavaScript interface

```ts
import { NativeModules } from 'react-native';

const { MyModule } = NativeModules;

MyModule.addNumbers(2, 3, (result) => {
    console.log(result); // prints 5
});
```