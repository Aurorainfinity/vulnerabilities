# 1. jpg file format

(c34.c8c): Access violation - code c0000005 (first chance)  
First chance exceptions are reported before any exception handling.  
This exception may be expected and handled.  
eax=13176ef6 ebx=0000000f ecx=000001ac edx=0000001d esi=04e09710 edi=0000000f  
eip=64343648 esp=0012f578 ebp=04e0939c iopl=0         nv up ei pl nz na pe nc  
cs=001b  ss=0023  ds=0023  es=0023  fs=003b  gs=0000             efl=00210206  
*** ERROR: Symbol file could not be found.  Defaulted to export symbols for   C:\Windows\WICCodecs\{A6D092A4-081A-4F0E-9356-DA167E87D922}\Raster   Formats\JPEG\x86\JPGCodec.dll -   
JPGCodec+0x753648:  
64343648 ff70fc          push    dword ptr [eax-4]    ds:0023:13176ef2=????????  
0:000> !exploitable -v  

!exploitable 1.6.0.0  
HostMachine\HostUser  
Executing Processor Architecture is x86  
Debuggee is in User Mode   
Debuggee is a live user mode debugging session on the local machine  
Event Type: Exception  
Exception Faulting Address: 0x13176ef2  
First Chance Exception Type: STATUS_ACCESS_VIOLATION (0xC0000005)  
Exception Sub-Type: Read Access Violation  

Faulting Instruction:64343648 push dword ptr [eax-4]  

Basic Block:  
    64343648 push dword ptr [eax-4]   
       Tainted Input operands: 'eax'  
    6434364b call dword ptr [jpgcodec!dllinstall+0x5078c (643a860c)]  
       Tainted Input operands: 'StackContents'   

Exception Hash (Major/Minor): 0x858b7aa7.0x434a582c  

 Hash Usage : Stack Trace:  
Major+Minor : JPGCodec+0x753648  
Major+Minor : JPGCodec!DllInstall+0xe321  
Major+Minor : Unknown  
Instruction Address: 0x0000000064343648     

Description: Data from Faulting Address is used as one or more arguments in a subsequent Function Call
Short Description: TaintedDataPassedToFunction  
Exploitability Classification: UNKNOWN  
Recommended Bug Title: Data from Faulting Address is used as one or more arguments in a subsequent  Function Call starting at JPGCodec+0x0000000000753648 (Hash=0x858b7aa7.0x434a582c)   