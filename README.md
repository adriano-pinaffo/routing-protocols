# Routing Protocols

This is a GNS3 project for the study of the following routing protocols: RIP, EIGRP, OSPF and BGP.
It also has configurations for DHCP and NAT.

### Project snapshot
![Architecture Overview](./overview.png)

### Items
Routers IOSv (Qemu)
images: vios-adventerprisek9-m.vmdk.SPA.156-1.T and vios-adventerprisek9-m.vmdk.SPA.156-2.T

Routers C3725 (dynamips)
image: c3725-adventerprisek9-mz.124-15.T14.image
Slots: WIC-2T

PCs (VPCS)

Ehternet Switches (default)

### Documentation
Accompanying documentation describing commands is provided. It contains a brief explanation of the protocols and their commands, caveats and configurations.

### How to use
Import the routing-protocols.gns3project file into your GNS3 version 1.5 or newer through File -> Import portable project...

### Known issues
2 images of IOSv were used. First, vios-adventerprisek9-m.vmdk.SPA.156-1.T was used for RIP and EIGRP blocks, but it has an identified bug that was fixed in version vios-adventerprisek9-m.vmdk.SPA.156-2.T. When the router is reboot the interfaces come back in shutdown mode, so it's necessary to manually bring them up. Once this was realized, OSPF block was created with the fixed version, but I haven't went back to fix RIP and EIGRP, forcing me to bring the interfaces up every time I restart the router. The file .gns3 can probably be changed to have the newer configuration but that was not tested yet.

Another thing, which is not really an issue, is that IOSV doesn't support slots, so the routers in dynamips were added to have serial link support.

### Acknowledgement
Keith Barker from CBT Nuggets, Ryan Lindfield, Vambar, David Bombal, and others

### Lincence and bug reporting

Enjoy and report bugs to https://github.com/adriano-pinaffo/routing-protocols/issues

This is a free project to be used as you like as long as you abide by CC0-1.0.
https://choosealicense.com/licenses/cc0-1.0/
