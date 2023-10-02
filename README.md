# usd-mpcdi-plugin
An OpenUSD plugin for the MPCDI VESA standard.

MPCDI is a VESA interchange format for videoprojectors technical data.

# Requirements
1. An USD Installation (tested with USD 22.11 and above)
2. CMake

# Build Instructions
1. `cmake . -DPXR_PATH=PATH_TO_USD_INSTALL`
2. Open the generated `.sln` file and compile.

# Building for Omniverse
An Omniverse extension uses this usd-mpcdi-plugin as a submodule, offering an alternative build procedure to compile using NVIDIA's USD (nv-usd). 

https://github.com/MomentFactory/Omniverse-MPCDI-converter

## Resources
- [MPCDI Christie Digital Github](https://github.com/ChristieDigital/mpcdi/blob/master/MPCDI_explained.md)
- MPCDIv2 standard can be downloaded from [the VESA website](https://vesa.org/vesa-standards/)
- MPCDIv2 is under Copyright © 2013 – 2015 Video Electronics Standards Association. All rights reserved.