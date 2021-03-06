UW CubeSat Project Main Processor Codebase
==========================================

This is the source code repository of the software system
on the main processor, based on FreeRTOS.

Build Instructions
------------------

1. Git-clone the project repository.
2. Download a copy of [TI Code Composer Studio](http://processors.wiki.ti.com/index.php/Download_CCS). Make sure you have the full/90-day evauation license.
 1. If you don't perform this step, you can also change your license option later by clicking on "Free Licence" label on the status bar, and then select "Upgrade".
3. Install CCS. During installation, make sure **TI ARM compiler** and MSP432 libs are selected.
 1. If you forget to select TI ARM compiler during installation, you can get it after-the-fact by going to Help -> CCS App Center.
4. Import the project into CCS as **a CCS Project**.
5. In the Project Explorer, make sure the project title contains "[Active - Debug]". You may switch between build configuration by selecting the drop-down on the build toolbar button, and then select "Debug".

From there, you should be able to build the project sucessfully
using the Debug configuration. Debug is the recommended configuration for day-to-day development.
Release strips away the debug symbols and thus should only be used for actual releases.

If you encounter a problem, it's probably due to issues with
relative paths. Contact xkxx@ and we'll figure it out.

Code Organization
-----------------

### FreeRTOS/

Source code of FreeRTOS, the embedded operating system.
Currently tracking source release v.9.0.0

DO NOT MODIFY.
When a version of FreeRTOS is released, replace the content of
this directory, but otherwise make no further changes on the
code itself.

### system/

Build config specific to the IDE. Do not modify unless you know
what you are getting into.

### dirverlib/

MSP432 low-level libraries, from TI MSP432Ware.

DO NOT MODIFY.
