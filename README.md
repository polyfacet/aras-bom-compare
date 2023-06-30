# Aras BOM Compare

A Part BOM Compare implementation for Aras Innovator.
See old demo on [Bom Compare Demo (R11)](https://youtu.be/jsfyDUVPpqs?t=173)

## Install steps

To install both the Code Tree and an import is needed.

### Code Tree Installation

0. (If not running R2023) Recompile <https://github.com/hilleconsultit/hc_aras_core_lib> for your specific version and modify method-config.xml (compare modifications between method-config.xml and method-config_R2023 in this project)
1. Copy the Client folder located in src/webapp
2. Paste into Innovator-folder (default: C:\Program Files (x86)\Aras\Innovator\Innovator)

### Database Installation

1. Open up the Aras Package Import tool.
2. Enter your login credentials and click Login (root required)
3. Enter the package name in the TargetRelease field.
4. Enter the path to your local src/packages/hcaras/hcimports.mf file in the Manifest File field.
5. Select all packages in the Available for Import field.
6. Select Type = Merge and Mode = Thorough Mode.

## History/Background

This implementation was initially done 2016 in Aras Innovator R11 SP?
The core code of the compare in <https://github.com/hilleconsultit/hc_aras_core_lib> I wrote for another PDM/PLM system, SmarTeam, probably around 2010/2011.
SmarTeam mainly was based on a Rich Client and the basic customizations where done in their ".bs"-files, which is a super set of Visual Basic Script (.vbs). These could be extended to call compiled assemblies, these assemblies was back then naturally done in VB6. These where later converted to VB.NET code. And that is why the core code is written in VB.NET.
