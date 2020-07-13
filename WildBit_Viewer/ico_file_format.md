# 1.  ico file format

(df0.1188): Access violation - code c0000005 (first chance)  
First chance exceptions are reported before any exception handling.  
This exception may be expected and handled.  
eax=00000000 ebx=000211c0 ecx=1c921000 edx=0275a400 esi=0266dd10 edi=0000ee50  
eip=008e3ffe esp=0012f7bc ebp=0012fc8c iopl=0         nv up ei pl nz na pe nc  
cs=001b  ss=0023  ds=0023  es=0023  fs=003b  gs=0000             efl=00210206  
*** ERROR: Symbol file could not be found.  Defaulted to export symbols for Editor.exe -   
Editor!TMethodImplementationIntercept+0x4189c6:   
008e3ffe 668901          mov     word ptr [ecx],ax        ds:0023:1c921000=????  
0:000> !exploitable -v  

!exploitable 1.6.0.0  
HostMachine\HostUser  
Executing Processor Architecture is x86  
Debuggee is in User Mode  
Debuggee is a live user mode debugging session on the local machine  
Event Type: Exception  
*** ERROR: Symbol file could not be found.  Defaulted to export symbols for   C:\Windows\system32\kernel32.dll -   
Exception Faulting Address: 0x1c921000  
First Chance Exception Type: STATUS_ACCESS_VIOLATION (0xC0000005)  
Exception Sub-Type: Write Access Violation   

Faulting Instruction:008e3ffe mov word ptr [ecx],ax  

Exception Hash (Major/Minor): 0x439ec9fa.0xd3da6413   

 Hash Usage : Stack Trace:  
Major+Minor : Editor!TMethodImplementationIntercept+0x4189c6  
Major+Minor : Editor!TMethodImplementationIntercept+0x55548d   
Major+Minor : Editor!TMethodImplementationIntercept+0x5555bc  
Major+Minor : Editor!TMethodImplementationIntercept+0x5510a5  
Major+Minor : Editor!TMethodImplementationIntercept+0x5514a3  
Minor       : Editor!TMethodImplementationIntercept+0x74eeb9  
Minor       : Editor!TMethodImplementationIntercept+0x7455cb  
Minor       : Editor!TMethodImplementationIntercept+0x30a223    
Minor       : Editor!TMethodImplementationIntercept+0x3094f8  
Minor       : Editor!TMethodImplementationIntercept+0x77b249  
Minor       : kernel32!BaseThreadInitThunk+0x12   
Minor       : ntdll!__RtlUserThreadStart+0x70  
Minor       : ntdll!_RtlUserThreadStart+0x1b  
Instruction Address: 0x00000000008e3ffe   

Description: User Mode Write AV  
Short Description: WriteAV  
Exploitability Classification: EXPLOITABLE  
Recommended Bug Title: Exploitable - User Mode Write AV starting at   Editor!TMethodImplementationIntercept+0x00000000004189c6 (Hash=0x439ec9fa.0xd3da6413)  