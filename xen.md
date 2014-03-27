# Xen

Microkernel hypervisor. This sheet displays often-used cli targets for the xm command.


## Move into console

    xm console <domain_name>

## Retrieving information.

### General host information.

    xm info;


### List domains.

    xm info;


### Get realtime information for the domains and the host.

    xm top;


### List vcpu information for the domains.

    xm vcpu-list;


### Logs.

#### Xend's message buffer.

    xm dmesg;


#### Xend's log.

    xm log;
