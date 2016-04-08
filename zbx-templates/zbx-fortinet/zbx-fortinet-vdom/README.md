ZBX-FORTINET-VDOM
=================

This template use the FORTINET-CORE-MIB and FORTINET-FORTIGATE-MIB to discover and manage virtual domain on Fortinet devices.

Items
-----

  * Configuration of virtual domains
  * Current number of virtual domains
  * Maximum number of virtual domains
  * Discovery: operation mode of each virtual domain
  * Discovery: CPU usage of each virtual domain
  * Discovery: memory usage of each virtual domain
  * Discovery: active sessions on each virtual domain
  * Discovery: session setup rate on each virtual domain
  * Discovery: vCluster HA member state of each virtual domain

Triggers
--------

  * **[HIGH]** => Memory usage for each virtual domain exceeded 80%
  * **[HIGH]** => CPU usage for each virtual domain exceeded 80%
  * **[HIGH]** => An increase of 40% of active sessions for each virtual domain was detected
  * **[AVERAGE]** => Memory usage for each virtual domain exceeded 70%
  * **[AVERAGE]** => CPU usage for each virtual domain exceeded 60%
  * **[AVERAGE]** => An increase of 30% of active sessions for each virtual domain was detected
  * **[WARNING]** => Memory usage for each virtual domain exceeded 60%
  * **[WARNING]** => CPU usage for each virtual domain exceeded 50%
  * **[WARNING]** => An increase of 20% of active sessions for each virtual domain was detected

Graphs
------

  * Discovery: CPU usage for each virtual domain
  * Discovery: Memory usage for each virtual domain
  * Discovery: Sessions count for each virtual domain

Installation
------------

1. Add a value mapping named `FgBoolState` with the following values:
  * 1 => disabled
  * 2 => enabled
2. Add a value mapping named `FgOpMode` with the following values:
  * 1 => nat
  * 2 => transparent
3. Add a value mapping named `FgHaState` with the following values:
  * 1 => master
  * 2 => backup
  * 3 => standalone
4. Import **zbx-fortinet-vdom.xml** file into Zabbix.
5. Add to your host the **{$SNMP_COMMUNITY}** macro with your SNMP community as value.
6. Associate **ZBX-FORTINET-VDOM** template to the host.
 
### Requirements

This template was tested for Zabbix 3.0.0 and higher.

License
-------

This template is distributed under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the  License, or (at your option) any later version.

### Copyright

  Copyright (c) Jean-Jacques Martrès

### Authors
  
  Jean-Jacques Martrès
  (jjmartres |at| gmail |dot| com)
