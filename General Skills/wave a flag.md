## Write-Ups for PicoCTF solved by Ayu Amira

### Wave a flag

###### Tags: picoCTF 2021, General Skills | Author: SYREAL

### Description: 
Can you invoke help flags for a tool or binary? [This program](http://https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm "This program") has extraordinarily helpful information...

### Solution: 
I have used Kali Linux VirtualBox to solve this solution. After downloading this file, I checked first the file. By running this command :
```
┌──(kali㉿kali)-[~/Desktop]
└─$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=985d9586d46e8651ab66c2fbb5a5473492466aa3, with debug_info, not stripped

```
It shows as an executable file. And I used chmod +x to execute the file.  Then I have entered ./warm to read the file.
```
┌──(kali㉿kali)-[~/Desktop]
└─$ chmod +x warm    
                                                                                                                                                                                                                 
┌──(kali㉿kali)-[~/Desktop]
└─$ ./warm       
Hello user! Pass me a -h to learn what I can do!
                                                  
```
The instruction ask me to use the -h. So, I just enter this command :
```
┌──(kali㉿kali)-[~/Desktop]
└─$ ./warm -h
Oh, help? I actually dont do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}

```
It returns the flag.

### Flag: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
