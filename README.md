During the VM boot process, interrupt the boot and append kickstart options as follows at end of the kernel line

- - - -

inst.xtimeout=300 ksdevice=link inst.ks=http://XX.XX.XX.XX/kickstart.cfg ip=10.141.XX.29::10.141.XX.1:255.255.254.XX:host1.testdomain.com:<interface-name>:none

- - - -

With above kickstart option we are specifying timeout of 300 seconds, with ksdevice=link option we are picking the default physical device active for accessing kickstart file.

http://XX.XX.XX.XX/kickstart.cfg is the location where the kickstart file is accessible, it can be a webserver or some http share location.

In above kickstart append arguments replace hostname, gateway, interface name, netmask as needed.
