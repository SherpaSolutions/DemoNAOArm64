
# Usage

- Run pod install

- Open workspace

- Try to compile; an error occurs stating
`
In path/libNAOSDK.a(ALOHA_cli.o), building for iOS Simulator, but linking in object file built for iOS, file 'path/libNAOSDK.a' for architecture arm64
`

- Adding arm64 in excluded archs fixes the issue, but it is only a patch over the real issue here. Setting this configuration should not be required on a default project running on Apple Silicon hardware

- When setting this configuration, build and run the app on a simulator.

- A warning is printed in the console output:

`
Warning: Error creating LLDB target at path 'path/Library/Developer/Xcode/DerivedData/SampleStaticLibNAO-djtkfslpxjstgdhdxngpylrhusgb/Build/Products/Debug-iphonesimulator/SampleStaticLibNAO.app'- using an empty LLDB target which can cause slow memory reads from remote devices: the specified architecture 'arm64-*-*' is not compatible with 'x86_64-apple-ios16.2.0-simulator' in 'path/Library/Developer/Xcode/DerivedData/SampleStaticLibNAO-djtkfslpxjstgdhdxngpylrhusgb/Build/Products/Debug-iphonesimulator/SampleStaticLibNAO.app/SampleStaticLibNAO'
`