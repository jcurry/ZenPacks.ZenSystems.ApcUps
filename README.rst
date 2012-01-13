==========================
ZenPacks.ZenSystems.ApcUps
==========================


Description
===========

Provides support for APC UPS devices with component and performance information for batteries.

Components
==========
The ZenPack has the following new Device Class
    * /Devices/Power/UPS/ApcUps

    * Components are: 
        * ApcUpsBattery which has details for: 
            * Various elements of battery status 

    * Modeler plugins are:   
        * ApcUpsDeviceMap    
            * Gathers Hardware and Software manufacturer and product
            * Serial number
            * Total number of battery packs
            * Number of bad battery packs
            * Basic output status
        * ApcUpsBatteryMap    
            * Gathers battery data for status
            * Time on battery
            * Battery last replacement date
            * Battery replacement indicator

    * Device template ApcUps provides device-level performance information:    
        * Data Sources    
            * Voltage
            * Current
            * Remaining capacity and time
            * Temperature 
        * Thresholds    
            * Low capacity
            * Low time remaining
            * High temperature
        * Graph Definitions    
            * Voltage
            * Current
            * Remaining capacity
            * Remaining time
            * Temperature

    * Device template ApcUpsInsAndOuts provides specific input / output performance information:    
        * Data Sources    
            * Input frequency and voltage
            * Output frequency, voltage, load and current 
        * Thresholds    
            * High load
        * Graph Definitions    
            * Input frequency and voltage
            * Output frequency, voltage, load and current 

    * A separate APC UPS Information menu delivers tabular and graphical  information for the overall device

 

Requirements & Dependencies
===========================

    * Zenoss Versions Supported: 3.0
    * External Dependencies: The APC UPS MIB needs to be available on target devices
    * ZenPack Dependencies:
    * Note that the standard /Power/UPS device class needs to exist.  If not, recreate it.
    * Installation Notes: zopectl restart after installing this ZenPack.
    * Configuration: 

Download
========
Download the appropriate package for your Zenoss version from the list
below.

* Zenoss 3.0+ `Latest Package for Python 2.6`_

Installation
============
Normal Installation (packaged egg)
----------------------------------
Copy the downloaded .egg to your Zenoss server and run the following commands as the zenoss
user::

   zenpack --install <package.egg>
   zenhub restart
   zopectl restart

Developer Installation (link mode)
----------------------------------
If you wish to further develop and possibly contribute back to this 
ZenPack you should clone the git repository, then install the ZenPack in
developer mode::

   zenpack --link --install <package>
   zenhub restart
   zopectl restart

Configuration
=============

Tested with Zenoss 3.1 against APC UPS RT 5000 devices

Change History
==============
* 1.0
   * Initial Release
* 1.1
   * Some updates for extra debug
* 1.2
   * Transferred to new github methods

Screenshots
===========
|ApcUpsInfo|
|ApcUpsBatteriesComponent|


.. External References Below. Nothing Below This Line Should Be Rendered

.. _Latest Package for Python 2.6: https://github.com/jcurry/ZenPacks.ZenSystems.ApcUps/blob/master/dist/ZenPacks.ZenSystems.ApcUps-1.2-py2.6.egg?raw=true

.. |ApcUpsInfo| image:: http://github.com/jcurry/ZenPacks.ZenSystems.ApcUps/raw/master/screenshots/ApcUpsInformation.jpg
.. |ApcUpsBatteriesComponent| image:: http://github.com/jcurry/ZenPacks.ZenSystems.ApcUps/raw/master/screenshots/ApcUpsBatteries.jpg

                                                                        

