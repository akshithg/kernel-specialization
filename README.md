# Kernel Specialization

The general goal of this work is to provide a way to package an application and the Linux kernel in a small virtual machine that can be easily shipped. The main idea is to get LLVM IR code for the application and the kernel and apply the existing OCCAM tool to prune as much unnecessary functionality as possible. 

Most of the effort has been to get a full version of the kernel code in LLVM IR, and then try to slash it using OCCAM's _razor_.

The _kernel-to-bitcode_ directory contains scripts to build the Linux kernel and extract the bitcode in a way that makes it bootable when recompiled.

The _kernel-slashing_ directory contains scripts used to apply OCCAM's _razor_ on the kernel bitcode.

## Environment
All this was done inside a Virtual Machine running on VirtualBox 5.2.12. The OS used is Ubuntu 16.04.

---

This material is based upon work supported by the National Science Foundation under Grant [ACI-1440800](http://www.nsf.gov/awardsearch/showAward?AWD_ID=1440800). Any opinions, findings, and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the National Science Foundation.
