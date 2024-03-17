# Firework Igniter WiFi Test Code (Run on WiFi Test Board) 

The source contained within this repository is intended to run on the WiFi test board (rev A01).  The purpose of this code is to test features available on the firework igniter.  The targe processor is the ESP8266 SOM.   

### ARCHITECTURE ###
The ESP8266 SOM can be bootloaded over the USB-to-serial interface. The Arduino IDE shall be used during development.   

### TOOL SUITE ###

The source file(s) are to be compiled using Arduino IDE v1.8.8, or newer.    

It is necessary to include esp8266 libraries. First, it must be verified that the correct board manager URL is included under the preference window.  Navigate to *File > Preferences*, and add the following URL: http://arduino.esp8266.com/stable/package_esp8266com_index.json

After including the necessary board manager URL, navigate to *tools > board > boards manager*, and install "esp8266".  This package will be considered to be *written by the "community"*.

For the asynchronous web sever, two libraries need to be manually downloaded and added so that <ESPAsyncWebServer.h> and <ESPAsyncTCP.h> can be included.  These libraries cannot be added through the board manager using conventional methods.

For ESPAsyncWebServer, download the file here.  A .ZIP file will be downloaded: <br>
https://github.com/me-no-dev/ESPAsyncWebServer/archive/master.zip <br>


For ESPAsyncTCP library, download the file here. A .ZIP file will be downloaded: <br>>
https://github.com/me-no-dev/ESPAsyncTCP/archive/master.zip <br>

Inside the sketch (Arduino IDE opened), click the option to include a library by navigating to the following option: *Sketch > Include Library > Add .ZIP Library...*  This will need to be repeated for each library we wish to add.  
The folders, which should be included at `\Documents\Arduino\libraries`, may have the -master suffix, but that's okay, as the sketch appears to compile and function fine.


### COMPILING ###
The ESP12 Test Board utilizes a bare ESP8266 WiFi SOM.  For proper compilation, the target board shall be  *Generic ESP8266 Module*.  

### VERSIONS ###
* Since this is only test code, this repository was copied over from another repository, thus history and previous tags weren't retained.  

* v0.1.2.a -- A lot of button progress was made, but clicking on SUBMIT still doesn't properly submit the value.  In the form definition, it seems the page will become unresponsive if the method is defined to be POST instead of GET.

