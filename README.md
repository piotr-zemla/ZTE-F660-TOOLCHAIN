# ZTE-F660-TOOLCHAIN

> [!CAUTION]
> This toolchain doesn't yet produce programs that reliabily run on the ZTE F660!
> 
> It's a very crude and uneducated reverse engineering effort, any help would be greatly appereciated!

## Introduction
A Toolchain thats (meant to be) compatible with original Linux system found on ZTE F660 v2.2 GPON router. 

## Table of Contents
1. [Introdcution](#introduction)
2. [Current State](#current-state)
   - [CPU/Hardware Compatibility](#cpuhardware-compatibility)
   - [Linux Compatibility](#linux-compatibility)
3. [Utilities included in the Toolchain](#utilities-included-in-the-toolchain)

## Current State
**Experimental code!** Only one programs is really proven to work reliably, and even then it needs a lot of work to get it working.

### CPU/Hardware Compatibility
Below is an image showing a difference between an **Original** Package, and one that was **Compiled** with the toolchain.

![Screenshot of difference in readelf](/Screenshot_20231222_124910.png)

Not identical, but close enough for the Router to recognize it as an executable.

### Linux Compatibility
Barely any. The toolchain is built to support Linux 2.6.32.71. Which is the closest version to that found on the Router that crosstool-ng supports.

Anything but the Kernel should be considered completely unsupported, and a blessing in the offchance that it works.

## Utilities included in the Toolchain
|   | GCC | uClibc-ng | Kernel Headers | make |
| - | - | - | - | - |
| Version  | 13.2.0 | 1.0.43 | 2.6.32.71 | 4.3 |
| Desired Version | UNKNOWN | UNKNOWN | 2.6.30 | UNKNOWN |

