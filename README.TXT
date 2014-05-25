Vulnserver

Check the authors blog at http://grey-corner.blogspot.com/ for more information and updates to this software.

======================================================================
ABOUT THE SOFTWARE
======================================================================

Vulnserver is a multithreaded Windows based TCP server that listens for client connections on port 9999 (by default) and allows the user to run a number of different commands that are vulnerable to various types of exploitable buffer overflows.

This software is intended mainly as a tool for learning how to find and exploit buffer overflow bugs, and each of the bugs it contains is subtly different from the others, requiring a slightly different approach to be taken when writing the exploit.

Though it does make an attempt to mimic a (simple) legitimate server program this software has no functional use beyond that of acting as an exploit target, and this software should not generally be run by anyone who is not using it as a learning tool.

======================================================================
COMPILING THE SOFTWARE
======================================================================

Binaries have been provided in this package, however if you wish to compile the software from the provided source files instructions are included in the file COMPILING.txt.

======================================================================
RUNNING THE SOFTWARE
======================================================================

To run the software, simply execute vulnserver.exe.  The provided essfunc.dll library must be in a location where it can be found by vulnserver.exe - keeping both files in the same directory will usually work fine.

To start the server listening on the default port of 9999, simply run the executable, to use an alternate port, provide the port number as a command line parameter.

Once the software is running, simply connect to it on port 9999 using a command line client like netcat.  Issue a HELP command (case sensitive) to see what functions are supported and go from there....

Detailed instructions on how to exploit this software, or example exploit files have not been included with this package - this is to provide a challenge for those who want it and also a disincentive to cheat by peeking at the answer.  A series of artciles on how to discover and exploit the bugs in this program are planned in future however, to provide a pointer for those who just need a hint as well as to act as learning guides for those new to the subject of exploitation.

======================================================================
LICENSE
======================================================================

See LICENSE.txt.

======================================================================
WARNING!!!!
======================================================================

UNDER NO CIRCUMSTANCES SHOULD THIS SOFTWARE BE RUN ON ANY SYSTEM THAT IS CONNECTED TO AN UNTRUSTED NETWORK OR THAT PERFORMS CRITICAL FUNCTIONS.  THE AUTHOR IS NOT RESPONSIBLE FOR ANY DAMAGES THAT MAY OCCUR FROM USING THIS SOFTWARE IN THIS OR ANY OTHER MANNER.  USE AT YOUR OWN RISK.
