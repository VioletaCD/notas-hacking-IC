# Static ain't always noise
## Descripcipción
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/static)? This [BASH script](https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/ltdis.sh) might help!
## Pistas
- (None)
## Solucion
```
-SOLUCIÓN 1
Una forma sencilla de resolver es descargando el archivo static
Una vez descargado simplemente es abrir el archivo en un txt y dentro juntos con otros caracteres se encuentra la bandera integra

- SOLUCIÓN 2
                                                                           
┌──(kali㉿kali)-[~]
└─$ ls -l 
total 376
drwxr-xr-x 2 kali kali     4096 Mar 22 15:55 Desktop
drwxr-xr-x 2 kali kali     4096 Mar  9 00:35 Documents
drwxr-xr-x 2 kali kali     4096 Mar 22 18:22 Downloads
-rw-r--r-- 1 kali kali    14551 Oct 26  2020 file
-rw-r--r-- 1 kali kali   288827 Mar 22 15:39 flagout.txt
drwxrwx--- 1 root vboxsf      0 Mar  9 01:22 haking
-rw-r--r-- 1 kali kali      785 Mar 15  2021 ltdis.sh
drwxr-xr-x 2 kali kali     4096 Mar  9 00:35 Music
drwxr-xr-x 2 kali kali     4096 Mar  9 00:35 Pictures
drwxr-xr-x 2 kali kali     4096 Mar  9 00:35 Public
-rw-r--r-- 1 kali kali     8376 Mar 15  2021 static
drwxr-xr-x 2 kali kali     4096 Mar  9 00:35 Templates
-rw-r--r-- 1 kali kali      100 Mar 14 14:53 token
drwxr-xr-x 2 kali kali     4096 Mar  9 00:35 Videos
-rwxr-xr-x 1 kali kali    10936 Mar 15  2021 warm
-rw-r--r-- 1 kali kali    10936 Mar 15  2021 warm.1
                                                                           
┌──(kali㉿kali)-[~]
└─$ chmod +x ltdis.sh
                                                                           
┌──(kali㉿kali)-[~]
└─$ ./ltdis.sh
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
                                                                           
┌──(kali㉿kali)-[~]
└─$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
                                                                           
┌──(kali㉿kali)-[~]
└─$ ls   
Desktop      haking    static                    Videos
Documents    ltdis.sh  static.ltdis.strings.txt  warm
Downloads    Music     static.ltdis.x86_64.txt   warm.1
file         Pictures  Templates
flagout.txt  Public    token
                                                                           
┌──(kali㉿kali)-[~]
└─$ cat static.ltdis.stringss.txt
cat: static.ltdis.stringss.txt: No such file or directory
                                                                           
┌──(kali㉿kali)-[~]
└─$ cat static.ltdis.strings.txt 
    238 /lib64/ld-linux-x86-64.so.2
    361 libc.so.6
    36b puts
    370 __cxa_finalize
    37f __libc_start_main
    391 GLIBC_2.2.5
    39d _ITM_deregisterTMCloneTable
    3b9 __gmon_start__
    3c8 _ITM_registerTMCloneTable
    660 AWAVI
    667 AUATL
    6ba []A\A]A^A_
    6e8 Oh hai! Wait what? A flag? Yes, it's around here somewhere!
    7c7 ;*3$"
   1020 picoCTF{d15a5m_t34s3r_1e6a7731}
   1040 GCC: (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.0
   1671 crtstuff.c
   167c deregister_tm_clones
   1691 __do_global_dtors_aux
   16a7 completed.7698
   16b6 __do_global_dtors_aux_fini_array_entry
   16dd frame_dummy
   16e9 __frame_dummy_init_array_entry
   1708 static.c
   1711 __FRAME_END__
   171f __init_array_end
   1730 _DYNAMIC
   1739 __init_array_start
   174c __GNU_EH_FRAME_HDR
   175f _GLOBAL_OFFSET_TABLE_
   1775 __libc_csu_fini
   1785 _ITM_deregisterTMCloneTable
   17a1 puts@@GLIBC_2.2.5
   17b3 _edata
   17ba __libc_start_main@@GLIBC_2.2.5
   17d9 __data_start
   17e6 __gmon_start__
   17f5 __dso_handle
   1802 _IO_stdin_used
   1811 __libc_csu_init
   1821 __bss_start
   182d main
   1832 __TMC_END__
   183e _ITM_registerTMCloneTable
   1858 flag
   185d __cxa_finalize@@GLIBC_2.2.5
   187a .symtab
   1882 .strtab
   188a .shstrtab
   1894 .interp
   189c .note.ABI-tag
   18aa .note.gnu.build-id
   18bd .gnu.hash
   18c7 .dynsym
   18cf .dynstr
   18d7 .gnu.version
   18e4 .gnu.version_r
   18f3 .rela.dyn
   18fd .rela.plt
   1907 .init
   190d .plt.got
   1916 .text
   191c .fini
   1922 .rodata
   192a .eh_frame_hdr
   1938 .eh_frame
   1942 .init_array
   194e .fini_array
   195a .dynamic
   1963 .data
   1969 .bss
   196e .comment
                 
```
## Bandera
picoCTF{d15a5m_t34s3r_1e6a7731}
## Notas adicionales

## Referencias
https://www.youtube.com/watch?v=QLRpjgVLTF0