### This is Task 01 of the Eudyptula Challenge
```
Write a Linux kernel module, and stand-alone Makefile, that when loaded
prints to the kernel debug log level, "Hello World!"  Be sure to make
the module be able to be unloaded as well.

The Makefile should build the kernel module against the source for the
currently running kernel, or, use an environment variable to specify
what kernel tree to build it against.

Please show proof of this module being built, and running, in your
kernel.  What this proof is is up to you, I'm sure you can come up with
something.  Also be sure to send the kernel module you wrote, along with
the Makefile you created to build the module.

Remember to use your ID assigned to you in the Subject: line when
responding to this task, so that I can figure out who to attribute it
to.  You can just respond to the task with the answers and all should be
fine.

If you forgot, your id is "".  But of course you have not
forgotten that yet, you are better than that.
```


### My solution 
(with help from https://blog.sourcerer.io/writing-a-simple-linux-kernel-module-d9dc3762c234)

```
# make
# sudo insmod hello.ko
# dmesg
[...]
[  888.099194] Hello, World!

# sudo rmmod hello
# dmesg
[...]
[  897.977944] Goodbye, World!
```

<img width="1117" alt="image" src="https://user-images.githubusercontent.com/3091714/236864490-21f059ae-751d-45d6-8057-5b79218f30be.png">

