cups-indexbraille
=================

Very basic CUPS backed to use with IndexBraille AB Everest-D V4.

# PRE-INSTALL

Since the manufacturer doesn't provide an embosser for GNU/Linux but for Windows or OSX to use with this printer, it's necesary to configure it to be used via network. Please, refer to the [manual](http://www.indexbraille.com/en-us/support/downloads?c=2) for further assistance.  

# INSTALL

Simply copy `indexbraille` to `/usr/lib/cups/backend` (on Debian based distros) and make sure that the permissions are `744` and the owner is `root`. Then copy `conf/cups-indexbraille.conf` to `/etc/cups/` and complete with the `PrinterHost`.  
After the files are in the correct directory, it's necessary to restart the CUPS service.
  
TODO: An installer :-)

# CONFIGURE

In your CUPS front-end of choice in "Local Printers", select "IndexBraille" and complete the fields for the printer (Name, Description, Location, etc). When selecting the PPD file, simply choose "Generic" and "Raw Printer" (or "Generic PostScript Printer"). Then pick your "Media Size" (ie: A4), "Media Source" (Printer Default) and "2-sided printing".  
  
Done!  

# BUGS

This is an experimental software to provide a quick ~~hack~~solution to use this printer. Bugfixes will come as time goes by.

# ERRORS

In case the printer is not available, please make sure the permissions are correct; if not, search for an error in `/var/log/cups/error_log`.






