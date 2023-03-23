┌──(kali㉿kali)-[~]
└─$ cd Documents/forense/Glory\ of\ the\ Garden 
                                                                                 
┌──(kali㉿kali)-[~/Documents/forense/Glory of the Garden]
└─$ strings garden.jpg -n 20                        
Copyright (c) 1998 Hewlett-Packard Company
IEC http://www.iec.ch
IEC http://www.iec.ch
.IEC 61966-2.1 Default RGB colour space - sRGB
.IEC 61966-2.1 Default RGB colour space - sRGB
,Reference Viewing Condition in IEC61966-2.1
,Reference Viewing Condition in IEC61966-2.1
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
Here is a flag "picoCTF{more_than_m33ts_the_3y3657BaB2C}"
                                                                            
┌──(kali㉿kali)-[~/Documents/forense/Glory of the Garden]
└─$ strings garden.jpg -n 20 | grep pico
Here is a flag "picoCTF{more_than_m33ts_the_3y3657BaB2C}"
                                                                            
┌──(kali㉿kali)-[~/Documents/forense/Glory of the Garden]
