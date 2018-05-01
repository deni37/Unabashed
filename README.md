# Unabashed
Basic Bash scripting library

This is a collection of simple libraries designed to speed up scripting in Bash. Everything is broken into groups based on purpose. 
Source desired libraries into your Bash script for day-to-day Linux administration. Verifiy that the file loaded by testing with:
  [[ -n <VERIFY_VARIABLE> ]] || { exit-on-error }
  For example:
      [[ -s "/path/to/print.lib" ]] && . /path/to/print.lib
      [[ -n "$_Print_" ]] || { printf "Unable to load source file\n" >&2; exit 1; }
      
The VERIFY_VARIABLE, _Print_, will have a non-zero length if the file successfully sourced into your script. This is not initially
intended to be an entire framework but once enough library files have been uploaded additional framework elements will be added.
Initial testing has been done on Ubuntu 16.04 with Bash 4.3. 
