# App sandboxing

Here are some ideas of how to sandbox an application. Could be used for any application, not just `gngr`.

### Separate user
The simplest way to sandbox an app is to run it as a separate user in your operating system. However, this by itself may not be sufficient. The X-Windows systems on Linux is notoriously [leaky](http://theinvisiblethings.blogspot.in/2011/04/linux-security-circus-on-gui-isolation.html).

### Virtualization / Namespacing
This takes a little more time to setup but can be safer.

Here are some packaged solutions that address this at various levels:
* https://www.qubes-os.org/
* https://github.com/netblue30/firejail
* https://github.com/projectatomic/bubblewrap
* http://subuser.org/
* https://subgraph.com/

* http://pdos.csail.mit.edu/mbox/

### Further reading
* https://wiki.gnome.org/Projects/SandboxedApps