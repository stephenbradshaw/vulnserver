# Vulnserver Windows Service

Provides that ability to allow for integration into training environments, and the automation of auto-recovery after exploitation.

When run, it will only utilize the default port: ``9999``

To install and uninstall the program as a service, run the following:

``vulnserverService.exe install``  
``vulnserverService.exe uninstall`` 
- Ensure the Service is stopped prior to uninstall

## Steps for Compiling the Source Code:
A good guide to installing and setting up environmental variables:
``https://www.ics.uci.edu/~pattis/common/handouts/mingweclipse/mingw.html``

Once setup you can run the following from your powershell prompt:

Builds the Essential Function DLL:

``gcc.exe -c essfunc.c``  
``gcc -shared -o essfunc.dll essfunc.o '-Wl,--out-implib=libessfunc.a' '-Wl,--image-base=0x62500000'``

Builds the Vulnserver Service Executable and links to the DLL:

``gcc.exe vulnserverService.c -o vulnserverService.exe -lws2_32 ./libessfunc.a``

Sets the Auto Restart options for the Windows Service and Starts it:

``sc.exe failure vulnserverService actions="restart/60000/restart/60000/restart/60000" reset=4000``  
``Get-Service vulnserverService | Start-Service``
