# Precompiled libraries for ResInsight

This repo is used to host Windows binary dependencies for ResInsight. The files are uploaded to a release in this repo, and consumed when building ResInsight.

Build custom-opm-common in both _Debug_ and _Release_. Create `custom-opm-common.zip` containing
    
    custom-opm-common.lib
    custom-opm-common_debug.lib


The prebuild binaries can be consumed in a ResInsight build in CMake.
https://github.com/OPM/ResInsight/blob/459dea64c7a417f26343ccb064c3b4390a2ab609/CMakeLists.txt#L446

## History
2023.08 : Added support for node vector names

https://github.com/OPM/ResInsight
