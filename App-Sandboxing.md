# App sandboxing

Here are some ideas of how to sandbox an application. Could be used for any application, not just `gngr`.

### Separate user
The simplest way to sandbox an app is to run it as a separate user in your operating system. However, this by itself may not be sufficient. The X-Windows systems on Linux is notoriously [leaky](http://theinvisiblethings.blogspot.in/2011/04/linux-security-circus-on-gui-isolation.html).

### Virtualization
This takes a little more time to setup but is safer. You can use tools such as `VirtualBox` or `lxc` to create virtual machines.

Here are some packaged solutions that address this at various levels:
* https://www.qubes-os.org/
* http://subuser.org/
* https://subgraph.com/
* https://l3net.wordpress.com/projects/firejail/
* http://pdos.csail.mit.edu/mbox/

### Further reading
* https://wiki.gnome.org/Projects/SandboxedApps