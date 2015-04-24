# App sandboxing

Here are some ideas of how to sandbox an application.

### Separate user
The simplest way to sandbox an app is to run it as a separate user in your operating system.

### Virtualization
This takes a little more time to setup but is safer. You can use tools such as `VirtualBox` or `lxc` to create virtual machines. 

### AOT code verifiction (like NaCl)
This means that Java Bytecode is recompiled into Java Bytecode while verifying that it does nothing nasty. The quasar fiber library does this using the ADM library in order to enforce cooperative multitasking (fibers). It appears Stanford researched this ages ago (theory.stanford.edu/~jcm/software/bytecode.html).

There are two benefits with this method. First of all it checks/modifies the code before runtime therefore not significantly impacting runtime performance. Call to "unsafe" code outside the sandbox can be redirected to code that is designed to be safe, or flat out replaced with code that throws a security exception. This will likely be faster than the standard Java Sandbox where it is the responsibility of a called method to check the callers security context, also it's probably safer as new Java functions that haven't been white-listed will be unavailable. Secondly it doesn't require any hardware features, which VirtualBOX or lxc-like containers do. 

Additionally this could be implemented as an extension to the Quasar library which also brings in fast multitasking capabilities.