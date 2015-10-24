#Build Configurations

Build Configurations enable developers to compile and build the code with different options depending on the build's purpose. By default Xcode projects come prepopulated with two build configurations, debug and release. Most of the time, these two standards build configurations are sufficient for any development project, however Xcode gives developers the ability to create additional custom build configurations.

The debug and release configuration settings are very similar, but the debug build configuration has a few settings that aid developers during the development and debugging stages of the software life cycle.

###Differences between debug and release build configurations

1. Build Active Architecture Only  
  * Debug = Yes  
  * Release = No  
2. Strip Debug Symbols During Copy  
  * Debug = No  
  * Release = Yes  
3. Apple LLVM 7.0 - Code Generation: Optimization Level  
  * Debug = None [-O0]  
  * Release = Fastest, Smallest [-Os]  
4. Swift Compiler - Code Generation: Optimization Level  
  * Debug = None [-Onone]  
  * Release = Fast [-O]  

The debug build configuration sets the **Build Active Architecture Only** option to Yes. This means that the compiler detects which specific physical device (or Simulator) is connected and builds the binary for only that architecture. This results in a faster build compared to the release build configuration which requires all supported architectures to be built into the binary, so that the app can be run on any supported devices.  
[iOS Developer Library: Xcode Build Setting Reference](https://developer.apple.com/library/ios/documentation/DeveloperTools/Reference/XcodeBuildSettingRef/1-Build_Setting_Reference/build_setting_ref.html#//apple_ref/doc/uid/TP40003931-CH3-SW157)  

**[Debug symbols](https://en.wikipedia.org/wiki/Debug_symbol)** serve as a link between the source code and the app binary, assisting in the debugging workflow and allowing for the symbolication of a crash log. If these symbols are stripped from the binary, then the crash report is likely to be meaningless to the developer. The debug build configuration keeps these symbols for these reasons. The release build configuration strips the debug symbols so as to keep the binary small as well as for security purposes. The debug symbols are saved in a separate DWARF dSYM file so that the developer can interpret user crash logs.  
[iOS Developer Library: Xcode Build Setting Reference](https://developer.apple.com/library/ios/documentation/DeveloperTools/Reference/XcodeBuildSettingRef/1-Build_Setting_Reference/build_setting_ref.html#//apple_ref/doc/uid/TP40003931-CH3-SW144)  

**Code optimizations** result in a smaller, faster binary but take longer to compile. For this reason, the debug build configuration by default disables optimizations so that the developer's build iterations can be as fast as possible. The release build configuration set the optimatization levels to fast and small by default so that the binary delivered to the user can occupy the least amount of space and run as fast as possible.  
*Reference*: [Mac Developer Library: Tuning for Performance and Responsiveness](https://developer.apple.com/library/ios/documentation/General/Conceptual/MOSXAppProgrammingGuide/Performance/Performance.html)  

###Creating a build configuration


*Reference*: [iOS Developer Library: Adding a Build Configuration](https://developer.apple.com/library/ios/recipes/xcode_help-project_editor/Articles/BasingBuildConfigurationsonConfigurationFiles.html)
