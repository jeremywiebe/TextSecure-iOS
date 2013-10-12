# TextSecure for iOS

Currently in early development stage.

## Building

1) Clone the repo to a working directory

2) [CocoaPods](http://cocoapods.org) is used to manage dependencies. Pods are setup easily and are distributed via a ruby gem. Follow the simple instructions on the website to setup. After setup, run the following command from the toplevel directory of TextSecureiOS to download the dependencies for TextSecure iOS:

```
pod install
```
If you are having build issues, first make sure your pods are up to date
```
pod update
pod install
```
occasionally, CocoaPods itself will need to be updated. Do this with
```
sudo gem update
```

3) **Temporary** - Building OpenSSL manually. This step should be removed soon. The goal is to make a pod specification that builds OpenSSL during the `pod install` phase.

- Download the [latest sources](http://www.openssl.org/source/)
- Decompress and copy them in the `Libraries/src/` folder. 
- Run the bash script called `build-libssl.sh` from within `Libraries/`. It will build the necessary dependencies (may take a bit but go get a cup of coffee) and you should be ready to go.

4) Open the `TextSecureiOS.xcworkspace` in Xcode. **Note that for CocoaPods to work properly it is very important to always open the workspace and not the `.xcodeproj` file.** Build and Run and you are ready to go!

5) Debugging network calls. If you are contributing networked code, PonyDebugger is integrated in Debug mode of the application. Check out https://github.com/square/PonyDebugger#quick-start and easily debug network code from the iOS simulator

## Documentation


Looking for documentation? Check out the wiki!

https://github.com/WhisperSystems/TextSecure/wiki

## Contribute

At this early stage there are two primary developers of TextSecure iOS and as we move from the early stages to more advanced ones opportunities will abound to contribute to the core code base. We are particularly interested in support and contributions associated localization, code review, and automated testing. Please contact us.

## Code Conventions

We are trying to follow the [GitHub code conventions for Objective-C](https://github.com/github/objective-c-conventions) and we would really appreciate that pull requests do conform with those conventions. 

In addition to that, always add curly braces to your `if` conditionals, even if there is no `else`.

## Cryptography Notice

This distribution includes cryptographic software. The country in which you currently reside may have restrictions on the import, possession, use, and/or re-export to another country, of encryption software. 
BEFORE using any encryption software, please check your country's laws, regulations and policies concerning the import, possession, or use, and re-export of encryption software, to see if this is permitted. 
See <http://www.wassenaar.org/> for more information.

The U.S. Government Department of Commerce, Bureau of Industry and Security (BIS), has classified this software as Export Commodity Control Number (ECCN) 5D002.C.1, which includes information security software using or performing cryptographic functions with asymmetric algorithms. 
The form and manner of this distribution makes it eligible for export under the License Exception ENC Technology Software Unrestricted (TSU) exception (see the BIS Export Administration Regulations, Section 740.13) for both object code and source code.

## License

Copyright 2013 Whisper Systems

Licensed under the GPLv3: http://www.gnu.org/licenses/gpl-3.0.html
