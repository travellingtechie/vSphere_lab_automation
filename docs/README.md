## Ansible Install

## Preparation
Place necessary files in directory specified in vars.yaml
### vCenter
open ISO and upload vcsa/vCenter---.ova file to content library as vcsa8.ova
You'll have to extract the files from the ova, and modify two lines:
`tar xvf vcsa8.ova`
Edit these lines and set userConfigurable="true"
```
<Property ovf:key="guestinfo.cis.appliance.ntp.servers" ovf:type="string" ovf:userConfigurable="false" ovf:value="">
<Property ovf:key="guestinfo.cis.deployment.autoconfig" ovf:type="boolean" ovf:userConfigurable="false" ovf:value="false">
```
Create a new ova
`tar cvf vcsa8-files.ova VMware-vCenter-Server-Appliance-8.0.0.10000-20519528_OVF10*`

### ESXi
download from https://williamlam.com/nested-virtualization/nested-esxi-virtual-appliance

### Ubuntu template
Install ubuntu minimal
create default user of ansible
install open-vm-tools
install ssh public key for ansible user 

### Windows template
download win2022 evaluation iso
create template win2022-template
Boot
