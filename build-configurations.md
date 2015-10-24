#Build Configurations

Build Configurations enable developers to compile and build the code with different options depending on the build's purpose. By default Xcode projects come prepopulated with two build configurations, debug and release. Most of the time, these two standards build configurations are sufficient for any development project, however Xcode gives developers the ability to create additional custom build configurations.

The debug and release configuration settings are very similar, but the debug build configuration has a few settings that aid developers during the development and debugging stages of the software life cycle:  

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


###Creating a build configuration


*Reference*: [iOS Developer Library: Adding a Build Configuration](https://developer.apple.com/library/ios/recipes/xcode_help-project_editor/Articles/BasingBuildConfigurationsonConfigurationFiles.html)
