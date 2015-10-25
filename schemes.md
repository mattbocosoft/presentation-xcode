#Xcode Schemes

A scheme is a higher-level of abstraction on top of build configurations and is an important part of the continuous integration workflow. *"An Xcode scheme defines a collection of targets to build, a configuration to use when building, and a collection of tests to execute."*  This means that a single scheme can define the entire integration process.

For example, a development team might create the following schemes:  

**Debugging Scheme**  
Developers can use this scheme to build and debug the app locally on the simulator or a their development device.  
  * Uses debug build configuration  
  * Uses development provisioning profile  

**Continuous Integration Scheme**  
Xcode Server can point to this scheme to build and distribute the app to QA on whatever any supported device.  
  * Uses release build configuration  
  * Uses adhoc provisioning profile  
  * Runs a set of test cases  


**Early-Adopter Scheme**  
This scheme would be used for generating an early-adopter build, potentially at the end of each Agile iteration, to send to customers and/or end-users.  
  * Uses release build configuration  
  * Uses adhoc provisioning profile


**App Store Scheme**  
At the end of an Agile release, this scheme is ready with the right certificate and distribution provisioning profile to build a binary and upload it to the App Store.  
  * Uses release build configuration  
  * Uses app store provisioning profile  


With this set of schemes, the team has a build workflow ready for each stage of the software life cycle.

**References**  
[1] [iOS Developer Library: Xcode Scheme](https://developer.apple.com/library/ios/featuredarticles/XcodeConcepts/Concept-Schemes.html)
