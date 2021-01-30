# esp_sdfat_wrap
This is a little helper library that wraps the popular SdFat library into Espressif's FS and File structures.

The wrapper idea came from: https://github.com/PaulStoffregen/SD.git

# Usage
Include the wrapper library into your project and make sure to "#include <sd_wrap.h>" instead of "SD.h"!
Now you can use the global variable *SDFAT* exactly like *SD*, for example for usage with the ESPAsyncWebServer, as *SDFAT* is an fs::FS structure, expected by many Espressif librarys.

If you want to keep the *SD* name, then change the define in "sd_wrap.h" accordingly and be sure that "SD.cpp" is not compiled by any of your used libraries!
