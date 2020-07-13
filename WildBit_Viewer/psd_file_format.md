# 1. psd file format; Editor!TMethodImplementationIntercept+0x53f6c3

(16e8.13b0): Access violation - code c0000005 (first chance)   
First chance exceptions are reported before any exception handling.  
This exception may be expected and handled.   
eax=12b21000 ebx=00000000 ecx=600c5ab7 edx=4aaaa5d7 esi=00000080 edi=00000000  
eip=00a0acfb esp=0012fbc0 ebp=0012fbc4 iopl=0         nv up ei pl nz na pe nc  
cs=001b  ss=0023  ds=0023  es=0023  fs=003b  gs=0000             efl=00210206  
*** ERROR: Symbol file could not be found.  Defaulted to export symbols for Editor.exe -   
Editor!TMethodImplementationIntercept+0x53f6c3:  
00a0acfb 8818            mov     byte ptr [eax],bl          ds:0023:12b21000=??  
0:000>!exploitable -v     

!exploitable 1.6.0.0  
HostMachine\HostUser  
Executing Processor Architecture is x86  
Debuggee is in User Mode  
Debuggee is a live user mode debugging session on the local machine  
Event Type: Exception  
*** ERROR: Symbol file could not be found.  Defaulted to export symbols for    C:\Windows\system32\kernel32.dll -  
Exception Faulting Address: 0x12b21000  
First Chance Exception Type: STATUS_ACCESS_VIOLATION (0xC0000005)  
Exception Sub-Type: Write Access Violation    

Faulting Instruction:00a0acfb mov byte ptr [eax],bl  

Exception Hash (Major/Minor): 0x439ec9fa.0x01e4ca09   

 Hash Usage : Stack Trace:   
Major+Minor : Editor!TMethodImplementationIntercept+0x53f6c3  
Major+Minor : Editor!TMethodImplementationIntercept+0x53fc50  
Major+Minor : Editor!TMethodImplementationIntercept+0x5405cd  
Major+Minor : Editor!TMethodImplementationIntercept+0x560662  
Major+Minor : Editor!TMethodImplementationIntercept+0x56035c  
Minor       : Editor!TMethodImplementationIntercept+0x551118  
Minor       : Editor!TMethodImplementationIntercept+0x5514a3  
Minor       : Editor!TMethodImplementationIntercept+0x74eeb9  
Minor       : Editor!TMethodImplementationIntercept+0x7455cb  
Minor       : Editor!TMethodImplementationIntercept+0x30a223  
Minor       : Editor!TMethodImplementationIntercept+0x3094f8  
Minor       : Editor!TMethodImplementationIntercept+0x77b249  
Minor       : kernel32!BaseThreadInitThunk+0x12   
Minor       : ntdll!__RtlUserThreadStart+0x70  
Minor       : ntdll!_RtlUserThreadStart+0x1b  
Instruction Address: 0x0000000000a0acfb    

Description: User Mode Write AV  
Short Description: WriteAV  
Exploitability Classification: EXPLOITABLE  
Recommended Bug Title: Exploitable - User Mode Write AV starting at      Editor!TMethodImplementationIntercept+0x000000000053f6c3 (Hash=0x439ec9fa.0x01e4ca09)   