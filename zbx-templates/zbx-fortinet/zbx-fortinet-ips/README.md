ZBX-FORTINET-IPS
================

This template use the FORTINET-CORE-MIB and FORTINET-FORTIGATE-MIB to discover and manage IPS activity.

Items
-----

  * Discovery: number of intrusions blocked for each virtual domain
  * Discovery: number of intrusions detected for each virtual domain

Triggers
--------

  * **[HIGH]** => An increase of 40% of detected intrusions for each virtual domain was detected
  * **[HIGH]** => An increase of 40% of blocked intrusions for each virtual domain was detected
  * **[AVERAGE]** => An increase of 30% of detected intrusions for each virtual domain was detected
  * **[AVERAGE]** => An increase of 30% of blocked intrusions for each virtual domain was detected
  * **[INFORMATION]** => An increase of 20% of detected intrusions for each virtual domain was detected
  * **[INFORMATION]** => An increase of 20% of blocked intrusions for each virtual domain was detected

Installation
------------

1. Import **zbx-fortinet-ips.xml** file into Zabbix.
2. Add to your host the **{$SNMP_COMMUNITY}** macro with your SNMP community as value.
3. Associate **ZBX-FORTINET-IPS** template to the host.
 
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
