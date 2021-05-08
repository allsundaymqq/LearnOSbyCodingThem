# LearnOSbyCodingThem
following Algorithman's series &lt;Write your own OS>

## Perface
Operating System, In my acknowage, is to get binaries to RAM and then tell CPU to run it.
so,I will document everything I learned from this series, this may not have profits for Others

## Tables of Contents
 - [Day1 Boot process and C++ stack Setup](#day1)
 
 
 
 <a name="day1"></a>
### Day1 Boot process and C++ stack Setup
1.Press the power button, then send singal to Mainboard, the BIOS inside of MB will do a POST( Power-On Self-Test), then do sth like check some Hardwares...  But BIOS is actually a ERPROM, have many firmwares(some binary codes for booting a OS).  
2.All we need to do, is to write OS code to BootLoader, it will load our code as an OS executed by CPU.      
  
Before we do that, C++ compiler output is not flat binaries, we have to write ASM code in the front of the OS code, so,  
The flat binaries, have two tasks, one is to tell the BootLoader load me As an OS, two is set up spaces for C++ call stack(about 2MB);  
When these two things over, we can now call OS.exe...  
  
In summarize, write ASM code and C++ code, then link them together to a .bin(Linux), copy the .bin file to /boot/ Dir. and modify the /boot/grub/grub.cfg file, add a new item for your OS.
