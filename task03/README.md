# Task 3 (2023)

### Build and boot custom kernel:
```
make -j 4
sudo make modules_install
sudo cp arch/arm64/boot/Image.gz /boot/vmlinuz-6.4.0-eudyptula\+
sudo cp System.map /boot/System.map-6.4.0-eudyptula\+
sudo kernel-install add 6.4.0-eudyptula\+ /boot/vmlinuz-6.4.0-eudyptula+
sudo reboot
```

<img width="1282" alt="image" src="https://user-images.githubusercontent.com/3091714/236885373-067400be-4dda-45ac-8705-297fff99be91.png">


### Patch:
```
diff --git a/Makefile b/Makefile
index 9d765ebcccf1..dc3ef22520d3 100644
--- a/Makefile
+++ b/Makefile
@@ -2,7 +2,7 @@
 VERSION = 6
 PATCHLEVEL = 4
 SUBLEVEL = 0
-EXTRAVERSION = -rc1
+EXTRAVERSION = -eudyptula
 NAME = Hurr durr I'ma ninja sloth

 # *DOCUMENTATION*
 ```


```
This is Task 03 of the Eudyptula Challenge
------------------------------------------

Now that you have your custom kernel up and running, it's time to modify
it!

The tasks for this round is:
  - take the kernel git tree from Task 02 and modify the Makefile to
    and modify the EXTRAVERSION field.  Do this in a way that the
    running kernel (after modifying the Makefile, rebuilding, and
    rebooting) has the characters "-eudyptula" in the version string.
  - show proof of booting this kernel.  Extra cookies for you by
    providing creative examples, especially if done in intrepretive
    dance at your local pub.
  - Send a patch that shows the Makefile modified.  Do this in a manner
    that would be acceptable for merging in the kernel source tree.
    (Hint, read the file Documentation/SubmittingPatches and follow the
    steps there.)

Remember to use your ID assigned to you in the Subject: line when
responding to this task, so that I can figure out who to attribute it
to.

If you forgot, your id is "".  Surely I don't need to keep
saying this right?  I know, _you_ wouldn't forget, but someone else, of
course they would, so I'll just leave it here for those "others".
```
