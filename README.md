# Precompiled libraries for ResInsight

This repo is used to host Windows binary dependencies for ResInsight. The files are uploaded to a release in this repo, and consumed when building ResInsight.

The prebuild binaries can be consumed in a ResInsight build in CMake.
https://github.com/OPM/ResInsight/blob/459dea64c7a417f26343ccb064c3b4390a2ab609/CMakeLists.txt#L446

Build custom-opm-common in both _Debug_ and _Release_. Create `custom-opm-common.zip` containing
    
    custom-opm-common/custom-opm-common.lib
    custom-opm-common/custom-opm-common_debug.lib


## How to build OpenSSL 1.1.1
The QNetwork module of Qt5 is depending on OpenSSL 1.1.1. 

    Set the environment variables for Visual Studio x64
    
    git clone https://github.com/microsoft/vcpkg.git
    git checkout 6e8aaa76f89f7a99fbe2ba4333c61cf940cd8bc4
    vcpkg/bootstrap-vcpkg.bat
    .\vcpkg install openssl --triplet x64-windows

Binaries will be available at
    
    vcpkg\packages\openssl_x64-windows\bin\libcrypto-1_1-x64.dll 
    vcpkg\packages\openssl_x64-windows\bin\libssl-1_1-x64.dll 

## History
2024.06 : Improved EGrid reader in opm_common

2024.06 : Add OpenSSL 1.1.1

2023.08 : Added support for node vector names


https://github.com/OPM/ResInsight
