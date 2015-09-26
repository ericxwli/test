# Concerns About Java

## Why Java?
* Only cross-platform high-level language with a fully-functional GUI library (AWT + Swing).
* Automatic memory management and resource management.
* Strongly and Statically typed.
* Runtime Sandboxing, via the Security Manager.
* Good performance for long running applications such as a browser.
* Fully open-source. (C# was not open-source and cross-platform until recently).

## Is Java secure?
First, a clarification. Many people associate `Java` with `Java applets`, which have turned out to be a huge security concern.

However, the term `Java` has other meanings too. `Java Applications` are usually written in the `Java language`, which gets compiled to the `Java byte code` and then execute in the `Java Virtual Machine`.

`gngr` is written in the `Java language` and runs on a desktop (standard edition) `Java Virtual Machine`. It does *not* run as an applet nor does it support applets. The security of `Java applications` running on the `Java Virtual Machine` is very good; they don't suffer from common security vulnerabilities such as buffer overruns, or access to freed memory. They can also utilise the sandboxing mechanism, as `gngr` does.

Now, there have been vulnerabilities found in the past in the sandboxing mechanism, just like in many other software artifacts. And these vulnerabilities get fixed on a regular basis. (TODO: Add a link to java vulnerability search in NVD).

## Why Java, and not some other JVM language?
* We forked from Lobo browser which was written in Java
* Java has lesser run-time overheads than other JVM languages
* Java has a larger community

We are exploring alternatives, such as Scala, Kotlin, Ceylon, but don't want to rush into them right now. Also, Java 8 added support for Lambdas, which somewhat reduced the gap.

## Is Java fast?
An implementation in a high-level language with automatic memory management will always have some overhead compared to an implementation in a low-level language with manual memory management. However, for long running applications, the JIT compiler in Java has a pretty good track record of performance.

There many features in a modern JVM that help improve speed, such as profile guided JIT compilation, escape analysis, generation based heap allocation and garbage collection, etc.

And there are ongoing efforts to make it even faster: [value objects](http://openjdk.java.net/jeps/169) and [module system](http://openjdk.java.net/projects/jigsaw/spec/sotms/).

# General

## Why does `gngr` block Cookies and Javascript by default?

Those technologies are a major concern from a security and privacy perspective. Cookies allow servers, especially third parties, to track you. Javascript opens up an even larger avenue for tracking and finger-printing, while also opening up a huge surface for attack.

Apart from the security concerns, executing javascript by default consumes more power, which is especially significant on mobile devices. 

That said, `gngr` does allow you to change this policy, either globally or on a per-site basis, via the [[RequestManager]].

