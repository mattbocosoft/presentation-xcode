#Distribute  

When a build is ready to be distributed to some audience, it must be archived through Xcode. It is important to build and archive your app through a legitimate version of Xcode that was downloaded from the official Apple Developer's website instead of a mirror, otherwise you could be [introducing security concerns](https://developer.apple.com/news/?id=09222015a).  

The "Archive" operation can be accessed from Xcode's Product menu. When an archive successfully completes, Xcode will automaticall open the Organizer window.  

![distribute-organizer](images/distribute-organizer.png)  

From the Organizer window, builds can be directly uploaded to iTunes Connect using the "Upload to App Store..." button. In reality, Organizer does not submit the build to the App Store, but rather uploads the build to iTunes Connect which is the gateway to the App Store. iTunes Connect also serves as the interface to TestFlight, the beta build distribution platform created by Burstly and acquired by Apple in 2014. TestFlight allows developers to distribute builds both to internal and external beta testers, however external beta testing requires that the build first go through a review process.  

Click the "Export" button to create an archive that can be manually distributed via one of four deployment methods:  

![distribute-export-dialog](images/distribute-export-dialog.png)  

1. iOS App Store  
If you want to create the archive to submit through a different medium than Xcode, then you can export the build. This option is useful if the project is using some sort of automated build and submission process other than Xcode, like [Fastlane.tools](https://fastlane.tools). The build will be built using your App Store distribution certificate and provisioning profile. Note that you cannot use this option if you only have an Enterprise distribution license.  

2. Ad Hoc  
To distribute a release build for testing before submitting to the App Store, export using Ad Hoc. The build will be built using your App Store distribution certificate and provisioning profile.  

3. Enterprise  
To distribute an internal Enterprise release build, use this option. The build will be built using your Enterprise distribution certificate and provisioning profile. Note that you cannot use this option if you only have an App Store distribution license, and builds built using this option cannot be distributed outside of your organization else you risk violating Apple's terms.  

4. Development  
To distribute a development build for testing, export using development. The build will be built using a development certificate and provisioning profile.  
