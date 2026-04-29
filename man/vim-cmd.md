# vim-cmd

> Specialized command line utility used specifically for VMWare ESXi to manage virtual machines and host configurations.
> Open an SSH to the host to use these tools.

- Register a VM

`vim-cmd solo/registervm {{path/to/vmx/file}}`
`vim-cmd /solo/register {{path/to/vmx/file}}`

- Unregister a VM

`vim-cmd vmsvc/unregister {{vmID}}`

- Delete a VM

`vim-cmd vmsvc/destroy {{vmID}}`

- List all VMs on the host and their IDs

`vim-cmd vmsvc/getallvms [includeConfigNotAvailable]`

- List snapshots of VM

`vim-cmd vmsvc/get.snapshot {{vmid}}`

- Get the power state of a VM

`vim-cmd vmsvc/power.getstate {{vmID}}`

- Get the uptime for a VM

`vim-cmd vmsvc/get.summary {{vmID}} | grep uptimeSeconds`

- Power on a VM

`vim-cmd vmsvc/power.on {{vmID}}`

- Reboot the VM guest OS

`vim-cmd vmsvc/power.reboot {{vmID}}`

- Reset a VM

`vim-cmd vmsvc/power.reset {{vmID}}`

- Upgrade VMWare Tools of a VM

`vim-cmd vmsvc/tools.upgrade vmID`

- Display the IP address of a VM

`vim-cmd vmsvc/get.guest {{vmID}} | grep -m 1 "ipAddress = \"`

Additional commands under vim-cmd:

- combinersvc/
- hostsvc/
- proxysvc/
- vimsvc/
- hbrsvc/
- internalsvc/
- solo/

Run `vim-cmd help {{command}}` for any of the above to get more information on available subcommands.
