# turbo-module-sample

- A react native app built according to the [getting started instructions](https://reactnative.dev/docs/environment-setup?guide=native&platform=ios&package-manager=npm&os=macos#installing-dependencies)
- A turbo module set up according to [the guide here](https://reactnative.dev/docs/the-new-architecture/pillars-turbomodules#android).
  
Only the Android/Kotlin side is implemented in this example. The app does build and run, but I get this error in the logs: ` Execution failed for task ':app:configureCMakeDebug[arm64-v8a]'.`.

This is the exception I'm currently getting when attempting `yarn android`.

```bash
info Installing the app...
> Task :gradle-plugin:compileKotlin UP-TO-DATE
> Task :gradle-plugin:compileJava NO-SOURCE
> Task :gradle-plugin:pluginDescriptors UP-TO-DATE
> Task :gradle-plugin:processResources UP-TO-DATE
> Task :gradle-plugin:classes UP-TO-DATE
> Task :gradle-plugin:jar UP-TO-DATE
> Task :gradle-plugin:inspectClassesForKotlinIC UP-TO-DATE
> Task :app:buildCodegenCLI SKIPPED
> Task :app:generateCodegenSchemaFromJavaScript SKIPPED
> Task :app:generateCodegenArtifactsFromSchema SKIPPED
> Task :app:generateNewArchitectureFiles
> Task :app:generatePackageList
> Task :app:preBuild
> Task :app:preDebugBuild
> Task :rtn-calculator:buildCodegenCLI SKIPPED
> Task :rtn-calculator:generateCodegenSchemaFromJavaScript UP-TO-DATE
> Task :rtn-calculator:generateCodegenArtifactsFromSchema UP-TO-DATE
> Task :rtn-calculator:preBuild UP-TO-DATE
> Task :rtn-calculator:preDebugBuild UP-TO-DATE
> Task :rtn-calculator:compileDebugAidl NO-SOURCE
> Task :app:compileDebugAidl NO-SOURCE
> Task :rtn-calculator:packageDebugRenderscript NO-SOURCE
> Task :app:compileDebugRenderscript NO-SOURCE
> Task :app:generateDebugBuildConfig UP-TO-DATE
> Task :app:javaPreCompileDebug UP-TO-DATE
> Task :rtn-calculator:writeDebugAarMetadata UP-TO-DATE
> Task :app:checkDebugAarMetadata UP-TO-DATE
> Task :app:generateDebugResValues UP-TO-DATE
> Task :rtn-calculator:compileDebugRenderscript NO-SOURCE
> Task :rtn-calculator:generateDebugResValues UP-TO-DATE
> Task :rtn-calculator:generateDebugResources UP-TO-DATE
> Task :rtn-calculator:packageDebugResources UP-TO-DATE
> Task :app:mapDebugSourceSetPaths UP-TO-DATE
> Task :app:generateDebugResources UP-TO-DATE
> Task :app:mergeDebugResources UP-TO-DATE
> Task :app:createDebugCompatibleScreenManifests UP-TO-DATE
> Task :app:extractDeepLinksDebug UP-TO-DATE
> Task :rtn-calculator:extractDeepLinksDebug UP-TO-DATE
> Task :rtn-calculator:processDebugManifest UP-TO-DATE
> Task :app:processDebugMainManifest UP-TO-DATE
> Task :app:processDebugManifest UP-TO-DATE
> Task :app:processDebugManifestForPackage UP-TO-DATE
> Task :rtn-calculator:compileDebugLibraryResources UP-TO-DATE
> Task :rtn-calculator:parseDebugLocalResources UP-TO-DATE
> Task :rtn-calculator:generateDebugRFile UP-TO-DATE
> Task :app:processDebugResources UP-TO-DATE
> Task :rtn-calculator:generateDebugBuildConfig UP-TO-DATE
> Task :rtn-calculator:javaPreCompileDebug UP-TO-DATE
> Task :app:mergeDebugShaders UP-TO-DATE
> Task :app:compileDebugShaders NO-SOURCE
> Task :app:generateDebugAssets UP-TO-DATE
> Task :rtn-calculator:mergeDebugShaders UP-TO-DATE
> Task :rtn-calculator:compileDebugShaders NO-SOURCE
> Task :rtn-calculator:generateDebugAssets UP-TO-DATE
> Task :rtn-calculator:packageDebugAssets UP-TO-DATE
> Task :app:mergeDebugAssets UP-TO-DATE
> Task :app:compressDebugAssets UP-TO-DATE
> Task :app:processDebugJavaRes NO-SOURCE
> Task :rtn-calculator:processDebugJavaRes NO-SOURCE
> Task :app:checkDebugDuplicateClasses UP-TO-DATE
> Task :app:desugarDebugFileDependencies UP-TO-DATE
> Task :app:mergeExtDexDebug UP-TO-DATE

> Task :rtn-calculator:compileDebugKotlin
'compileDebugJavaWithJavac' task (current target is 11) and 'compileDebugKotlin' task (current target is 1.8) jvm target compatibility should be set to the same Java version.

> Task :app:configureCMakeDebug[arm64-v8a] FAILED
C/C++: CMake Error at /Users/basilshah/Desktop/untitled folder/AwesomeProject/android/app/build/generated/rncli/src/main/jni/Android-rncli.cmake:6 (add_subdirectory):
C/C++:   add_subdirectory called with incorrect number of arguments
C/C++: Call Stack (most recent call first):
C/C++:   /Users/basilshah/Desktop/untitled folder/AwesomeProject/node_modules/react-native/ReactAndroid/cmake-utils/ReactNative-application.cmake:121 (include)
C/C++:   CMakeLists.txt:31 (include)
C/C++: CMake Error at /Users/basilshah/Desktop/untitled folder/AwesomeProject/node_modules/react-native/ReactAndroid/cmake-utils/ReactNative-application.cmake:124 (target_link_libraries):
C/C++:   Cannot specify link libraries for target "react_codegen_RTNCalculatorSpec"
C/C++:   which is not built by this project.
C/C++: Call Stack (most recent call first):
C/C++:   CMakeLists.txt:31 (include)
41 actionable tasks: 4 executed, 37 up-to-date

info 💡 Tip: Make sure that you have set up your development environment correctly, by running react-native doctor. To read more about doctor command visit: https://github.com/react-native-community/cli/blob/main/packages/cli-doctor/README.md#doctor 


FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:configureCMakeDebug[arm64-v8a]'.
> [CXX1429] error when building with cmake using /Users/basilshah/Desktop/untitled folder/AwesomeProject/node_modules/react-native/ReactAndroid/cmake-utils/default-app-setup/CMakeLists.txt: -- The C compiler identification is Clang 12.0.8
  -- The CXX compiler identification is Clang 12.0.8
  -- Detecting C compiler ABI info
  -- Detecting C compiler ABI info - done
  -- Check for working C compiler: /Users/basilshah/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/bin/clang - skipped
  -- Detecting C compile features
  -- Detecting C compile features - done
  -- Detecting CXX compiler ABI info
  -- Detecting CXX compiler ABI info - done
  -- Check for working CXX compiler: /Users/basilshah/Library/Android/sdk/ndk/23.1.7779620/toolchains/llvm/prebuilt/darwin-x86_64/bin/clang++ - skipped
  -- Detecting CXX compile features
  -- Detecting CXX compile features - done
  -- Configuring incomplete, errors occurred!
  See also "/Users/basilshah/Desktop/untitled folder/AwesomeProject/android/app/.cxx/Debug/4hy2d6k1/arm64-v8a/CMakeFiles/CMakeOutput.log".
  
  C++ build system [configure] failed while executing:
      /Users/basilshah/Library/Android/sdk/cmake/3.22.1/bin/cmake \
        "-H/Users/basilshah/Desktop/untitled folder/AwesomeProject/node_modules/react-native/ReactAndroid/cmake-utils/default-app-setup" \
        -DCMAKE_SYSTEM_NAME=Android \
        -DCMAKE_EXPORT_COMPILE_COMMANDS=ON \
        -DCMAKE_SYSTEM_VERSION=21 \
        -DANDROID_PLATFORM=android-21 \
        -DANDROID_ABI=arm64-v8a \
        -DCMAKE_ANDROID_ARCH_ABI=arm64-v8a \
        -DANDROID_NDK=/Users/basilshah/Library/Android/sdk/ndk/23.1.7779620 \
        -DCMAKE_ANDROID_NDK=/Users/basilshah/Library/Android/sdk/ndk/23.1.7779620 \
        -DCMAKE_TOOLCHAIN_FILE=/Users/basilshah/Library/Android/sdk/ndk/23.1.7779620/build/cmake/android.toolchain.cmake \
        -DCMAKE_MAKE_PROGRAM=/Users/basilshah/Library/Android/sdk/cmake/3.22.1/bin/ninja \
        "-DCMAKE_LIBRARY_OUTPUT_DIRECTORY=/Users/basilshah/Desktop/untitled folder/AwesomeProject/android/app/build/intermediates/cxx/Debug/4hy2d6k1/obj/arm64-v8a" \
        "-DCMAKE_RUNTIME_OUTPUT_DIRECTORY=/Users/basilshah/Desktop/untitled folder/AwesomeProject/android/app/build/intermediates/cxx/Debug/4hy2d6k1/obj/arm64-v8a" \
        -DCMAKE_BUILD_TYPE=Debug \
        "-DCMAKE_FIND_ROOT_PATH=/Users/basilshah/Desktop/untitled folder/AwesomeProject/android/app/.cxx/Debug/4hy2d6k1/prefab/arm64-v8a/prefab" \
        "-B/Users/basilshah/Desktop/untitled folder/AwesomeProject/android/app/.cxx/Debug/4hy2d6k1/arm64-v8a" \
        -GNinja \
        "-DPROJECT_BUILD_DIR=/Users/basilshah/Desktop/untitled folder/AwesomeProject/android/app/build" \
        "-DREACT_ANDROID_DIR=/Users/basilshah/Desktop/untitled folder/AwesomeProject/node_modules/react-native/ReactAndroid" \
        -DANDROID_STL=c++_shared \
        -DANDROID_USE_LEGACY_TOOLCHAIN_FILE=ON
    from /Users/basilshah/Desktop/untitled folder/AwesomeProject/android/app
  CMake Error at /Users/basilshah/Desktop/untitled folder/AwesomeProject/android/app/build/generated/rncli/src/main/jni/Android-rncli.cmake:6 (add_subdirectory):
    add_subdirectory called with incorrect number of arguments
  Call Stack (most recent call first):
    /Users/basilshah/Desktop/untitled folder/AwesomeProject/node_modules/react-native/ReactAndroid/cmake-utils/ReactNative-application.cmake:121 (include)
    CMakeLists.txt:31 (include)
  
  
  CMake Error at /Users/basilshah/Desktop/untitled folder/AwesomeProject/node_modules/react-native/ReactAndroid/cmake-utils/ReactNative-application.cmake:124 (target_link_libraries):
    Cannot specify link libraries for target "react_codegen_RTNCalculatorSpec"
    which is not built by this project.
  Call Stack (most recent call first):
    CMakeLists.txt:31 (include)

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 3s
info Run CLI with --verbose flag for more details.

```

This is what I get when running `yarn react-native doctor`

```
Common
 ✓ Node.js - Required to execute JavaScript code
 ✓ yarn - Required to install NPM dependencies
 ✓ Watchman - Used for watching changes in the filesystem when in development mode

Android
 ✓ Adb - Required to verify if the android device is attached correctly
 ✓ JDK - Required to compile Java code
 ✓ Android Studio - Required for building and installing your app on Android
 ✓ Android SDK - Required for building and installing your app on Android
 ✓ ANDROID_HOME - Environment variable that points to your Android SDK installation

iOS
 ✓ Xcode - Required for building and installing your app on iOS
 ✓ Ruby - Required for installing iOS dependencies
 ✓ CocoaPods - Required for installing iOS dependencies
 ✓ ios-deploy - Required for installing your app on a physical device with the CLI
 ✓ .xcode.env - File to customize Xcode environment

Errors:   0
Warnings: 0

```
