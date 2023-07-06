# Detailed process statistics on Cacti via SNMP (processes+)

Standard SNMP provides statistics on processes, but what is very useful is to know the process state. These can give valuable diagnostic information such as an IO problem resulting in many processes in Uninterruptible Sleep, or a bug resulting in many Zombie processes.

This is a tiny snmpd extension with Cacti graph to do just that - effectively an enhanced version of the standard processes graph.

## ps to SNMP

Place the script **procs-stats** in a suitable place (eg. /etc/snmp) and add the config from snmpd.conf.cacti-processes+ to your **/etc/snmp/snmpd.conf**, restarting snmpd after.

## SNMP to Cacti

At this point your Cacti host definition needs to be working for SNMP and you should be able to simply import the template **cacti_host_template_processes.xml** and add the graph.
