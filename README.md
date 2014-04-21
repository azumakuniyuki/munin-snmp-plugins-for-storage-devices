Munin SNMP Plugins for storage devices
======================================

Plugins for EqualLogic
----------------------
Munin plugins for EqualLogic via SNMP. These plugins require entries in /etc/hosts
like followings:

    # cat /etc/hosts
    192.168.0.101 eq01
    192.168.0.102 eq02
    ...

## snmp\_\_equallogic\_cache
Storage cache statistics

### Setup

    # cd /etc/munin/plugins
    # for E in eq01 eq02; do
    > ln -s /usr/share/munin/plugins/snmp__equallogic_storage ./snmp_${E}_equallogic_storage
    > done

## snmp\_\_equallogic\_conn
Information about connections

### Setup

    # cd /etc/munin/plugins
    # for E in eq01 eq02; do
    > ln -s /usr/share/munin/plugins/snmp__equallogic_conn ./snmp_${E}_equallogic_conn
    > done

## snmp\_\_equallogic\_diskerror\_
Error counts of each disk in EqualLogic

    # cd /etc/munin/plugins
    # echo 'Substitute the ERROR NAME for variable "X"'
    # X=internal
    # for E in eq01 eq02; do
    > ln -s /usr/share/munin/plugins/snmp__equallogic_diskerror_ ./snmp_${E}_equallogic_diskerror_$X
    > done

## snmp\_\_equallogic\_diskstatus_
Status of each disk in EqualLogic

### Setup
    # cd /etc/munin/plugins
    # echo 'Substitute the STATUS NAME for variable "X"'
    # X=xfer
    # for E in eq01 eq02; do
    > ln -s /usr/share/munin/plugins/snmp__equallogic_diskstatus_ ./snmp_${E}_equallogic_diskstatus_$X
    > done

## snmp\_\_equallogic\_fan
Fan RPMs in EqualLogic

### Setup
    # cd /etc/munin/plugins
    # for E in eq01 eq02; do
    > ln -s /usr/share/munin/plugins/snmp__equallogic_fan ./snmp_${E}_equallogic_fan
    > done

## snmp\_\_equallogic\_pool
Pool statistics in EqualLogic

### Setup
    # cd /etc/munin/plugins
    # for E in eq01 eq02; do
    > ln -s /usr/share/munin/plugins/snmp__equallogic_pool ./snmp_${E}_equallogic_pool
    > done

## snmp\_\_equallogic\_storage
Storage usage in EqualLogic

### Setup
    # cd /etc/munin/plugins
    # for E in eq01 eq02; do
    > ln -s /usr/share/munin/plugins/snmp__equallogic_storage ./snmp_${E}_equallogic_storage
    > done

## snmp\_\_equallogic\_temp
temperatures in EqualLogic

### Setup
    # cd /etc/munin/plugins
    # for E in eq01 eq02; do
    > ln -s /usr/share/munin/plugins/snmp__equallogic_temp ./snmp_${E}_equallogic_temp
    > done


Plugins for QNAP
----------------

## snmp\_\_qnap\_disk
Disk usage of QNAP NAS Stroage. This plugin does not work properly when the device 
returns negative value.

### Setup
    # cd /etc/munin/plugins
    # ln -s /usr/share/munin/plugins/snmp__qnap_disk ./snmp_qn1_qnap_disk

## snmp\_\_qnap\_fan
Fan RPMs in QNAP storage

### Setup
    # cd /etc/munin/plugins
    # ln -s /usr/share/munin/plugins/snmp__qnap_fan ./snmp_qn1_qnap_fan

## snmp\_\_qnap\_temp
Temperatures in QNAP NAS storage

### Setup
    # cd /etc/munin/plugins
    # ln -s /usr/share/munin/plugins/snmp__qnap_temp ./snmp_qn1_qnap_temp

SEE ALSO
--------
* [SNMP OID for EqualLogic](http://cric.grenoble.cnrs.fr/Administrateurs/Outils/MIBS/?oid=1.3.6.1.4.1.12740)
* [QNAP Turbo NAS Software User Manual](http://docs.qnap.com/nas/en/index.html?snmp_settings.htm)

