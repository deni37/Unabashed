# Unabashed
Basic Bash scripting library

This is a collection of simple libraries designed to speed up scripting in Bash. Everything is broken into groups based on purpose.

SCRIPTING USE
-------------
Source desired libraries into your Bash script for day-to-day Linux administration. Verify that the file loaded by testing with:

  [[ -n <VERIFY_VARIABLE> ]] || { exit-on-error }

  For example:
  
      [[ -s "/path/to/print.lib" ]] && . /path/to/print.lib
      
      
      [[ -n "$_Print_" ]] || { printf "Unable to load source file\n" >&2; exit 1; }


In the example the VERIFY_VARIABLE, \_Print\_, will have a non-zero length if the file successfully sourced into your script.

FRAMEWORK USE
-------------
To use this as a framework follow these steps:

  1)  Place the Unabashed library in the "/home" directory resulting in "/home/Unabashed"
  2)  Place the following line at the end of either /home/\<USER\>/.bashrc, /home/\<USER\>/.profile, or /etc/profile:
  
     \#\#!!!!!!!!!!!!!!!!!!!!!!!!##
     \#\# LOAD Unabashed LIBRARY ##      
     \#\#!!!!!!!!!!!!!!!!!!!!!!!!##      
     if [ -e /home/Unabashed/.pref ]      
        then
          . /home/Unabashed/.pref          
     fi
  
You can verfiy that the library has loaded by running:
     
     echo $UnabashedVersion
     
Initial testing has been done on Ubuntu 16.04 with Bash 4.3. 
