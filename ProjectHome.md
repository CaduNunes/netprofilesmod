<font color='red' size='5'><b>Google Code is shutting down and the project is now hosted on <a href='https://github.com/geissbuehler/netprofilesmod'>GitHub</a>.</b></font>

# Net Profiles <sup>mod</sup> #

A fork of the abandoned project [Net Profiles](http://code.google.com/p/netprofiles/).

![http://wiki.netprofilesmod.googlecode.com/git/images/main_screen_win8.png](http://wiki.netprofilesmod.googlecode.com/git/images/main_screen_win8.png)

Net Profiles <sup>mod</sup> saves your network settings in profiles and allows to apply these settings with a click of a button. The project is entirely developed with [SharpDevelop](http://www.icsharpcode.net/opensource/sd/). Net Profiles <sup>mod</sup> is free software and is licensed under the [GNU General Public License (GPL) 3.0](http://www.gnu.org/licenses/gpl-3.0).

## Features ##

The following options are supported in profiles:
  * DHCP or static network configuration, including support for WINS server and DNS suffix.
  * Proxy settings for Internet Explorer and Firefox, with separate proxy settings per protocol (http, https, ftp, socks, gopher) and proxy exceptions. To apply new proxy settings, Firefox is automatically restarted with the last session restored.
  * Network drives to be connected on profile activation.
  * The default printer.
  * Programs to be executed on activation.
  * The desktop wallpaper and resolution.
  * A wireless SSID to automatically activate the profile when the specified wireless network is connected.

Additional features:
  * Multi language support.
  * Supports creation of shortcuts for direct activation of a specific profile.
  * Can be minimized to tray. The tray context menu allows to directly apply profiles.
  * Optionally start with Windows, optionally start minimized/trayed.

## System Requirements ##

  * Windows XP, Vista, 7 or 8 (corresponding server variants not tested very well, but should work as well)
  * .NET Framework 2.0 ([installing .NET 2.0 on Windows 8](http://helpdeskgeek.com/windows-8/install-net-framework-3-5-3-0-2-0-on-windows-8/))

## Version History ##

### 0.2.4 (18 April 2015) ###
  * Reflect migration to GitHub
  * Sort profiles by name
  * Sort adapters by name
  * No flickering when loading profiles
  * Show detailed error message when applying IP settings fails

### 0.2.3 (16 February 2014) ###

Bug fixes:
  * Allow installation on Windows 8.1 (installer no more checks maximum Windows version)
  * Fixed broken compatibility with Windows Sever 2008 and newer

### 0.2.2 (20 May 2013) ###

Bug fixes:
  * Fixed the increased CPU load by scanning the available network adapters in the background (using a NetworkAvailabilityChanged handler instead of periodically scanning the adapters)
  * No exception on Vista and newer if no WLAN adapter is installed in the system

### 0.2.1 (10 May 2013) ###

Bug fixes:
  * Application is no more blocking while activating a profile (applied in a separate thread)
  * No more lags of the user interface caused by scanning the available adapters in the background (runs in a separate thread instead of using a timer)

### 0.2.0 (01 May 2013) ###

New features:
  * Automatic profile activation on connected SSID now also works on Vista and newer
  * The network adapter list is now automatically updated in the background (automatic activation on connected wireless SSID is now really automatically)
  * Added an option for disabling to ask for confirmation before restarting Firefox when applying proxy settings
  * No more filtering of available display resolutions for rather low 'standard resolutions', only resolutions below 640 x 480 are filtered
  * Retrieving of available display resolutions from the system now also works on Windows 8 (dropped the support for setting the color depth in the profile)

Bug fixes:
  * The display resolution is now saved language independent in the profile file
  * No more exceptions when creating a new profile while no connected adapter is available
  * No more exceptions from improper formatted proxy exception settings

### 0.1.1 (21 December 2012) ###

  * Fixed an error that prevented installation on non-English systems
  * Proxy exceptions in the IE format with asterisks (`192.168.0.100;*.example.com;10.92.*`) are now converted to the format `192.168.0.100;.example.com;10.92.0.0/16` for the Firefox proxy configuration
  * Other bug fixes

### 0.1.0 (12 December 2012) ###

This is the first release of Net Profiles <sup>mod</sup> since it has been forked from the original Net Profiles. It is still beta software, but it should already be good enough as your daily driver.

New features compared to the original Net Profiles 2.1.8:
  * Added compatibility with Windows Vista, Windows 7 and Windows 8 (Win8 not tested very well yet)
  * Added a 64-bit edition
  * Fully compatible with Windows User Account Control: administrators are able to edit network profiles, users can only apply profiles (for applying profiles without elevated permissions, a service has been added)
  * Added support for DNS suffixes
  * Added support for proxy exceptions, for example `192.168.0.100;*.example.com;10.92.*` (`*` is ignored by Firefox, will be fixed in the next version)
  * Added support for separate proxy settings per protocol (http, https, ftp, socks, gopher) by entering a proxy address like `http=proxy.example.com:8080;ftp=127.0.0.1`
  * Adapted Firefox proxy settings for current Firefox versions
  * Removed obsolete support for proxy settings for Opera 6 and older (new Opera versions use Windows proxy settings)

Issues of Net Profiles closed in this first release of Net Profiles mod:
  * [5](http://code.google.com/p/netprofiles/issues/detail?id=5)
  * [24](http://code.google.com/p/netprofiles/issues/detail?id=24) (not 100% sure)
  * [30](http://code.google.com/p/netprofiles/issues/detail?id=30) (the code is now here ;) )
  * [34](http://code.google.com/p/netprofiles/issues/detail?id=34)
  * [41](http://code.google.com/p/netprofiles/issues/detail?id=41)
  * [54](http://code.google.com/p/netprofiles/issues/detail?id=54)
  * [14](http://code.google.com/p/netprofiles/issues/detail?id=14), [19](http://code.google.com/p/netprofiles/issues/detail?id=19),  [28](http://code.google.com/p/netprofiles/issues/detail?id=28), [50](http://code.google.com/p/netprofiles/issues/detail?id=50),  [53](http://code.google.com/p/netprofiles/issues/detail?id=53)