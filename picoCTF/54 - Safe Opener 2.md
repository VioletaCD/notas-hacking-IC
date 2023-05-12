# Safe Opener 2
## Descripcipción
What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/290/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
## Pistas
- Download and try to decompile the file..
## Solucion
```
_____________________________________________________________________________
									FORMA 1
_____________________________________________________________________________
┌──(kali㉿kali)-[~/Documents/reversing/safer]
└─$ ls
SafeOpener.class
┌──(kali㉿kali)-[~/Documents/reversing/safer]
└─$ file SafeOpener.class 
SafeOpener.class: compiled Java class data, version 52.0 (Java 1.8)
                                                                            
┌──(kali㉿kali)-[~/Documents/reversing/safer]
└─$ cat SafeOpener.class 
����4�
CDE     FG
H
I
JL      FN
OP
Q
RS
.T
OU
VW
X
Y
[
]
R`ab<init>()VCodeLineNumberTableLocalVariableTablethis
                                                      LSafeOpener;main([Ljava/lang/String;)VisOpenZargs[Ljava/lang/Stringkeyboard▒Ljava/io/BufferedReader;encodercEncoder
                 InnerClasses▒Ljava/util/Base64$Encoder;
StackMapTable*Dcdang/String;keyiI
ExceptionsopenSafe(Ljava/lang/String;)password
SourceFileSafeOpener.java
                         java/io/BufferedReaderjava/io/InputStreamReaderf
                                                                         gh
                                                                           i
jk
  lm
    noEnter password for the safe: p
                                    qr
                                      std
                                         uv
                                           wx
                                             yr
                                               >?java/lang/StringBuilder
You have  
          z{
            z| attempt(s) left
                              }t,picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}
 ~
  Sesame openPassword is incorrect

SafeOpenerjava/lang/Object▒java/util/Base64$Encoderjava/lang/Stringjava/io/IOExceptionjava/lang/SysteminLjava/io/InputStream;▒(Ljava/io/InputStream;)V(Ljava/io/Reader;)Vjava/util/Base64
getEncoder()Ljava/util/Base64$Encoder;outLjava/io/PrintStream;java/io/PrintStreamprint(Ljava/lang/String;)readLine()Ljava/lang/StringgetBytes()[BencodeToString([B)Ljava/lang/String;printlnappend-(Ljava/lang/String;)Ljava/lang/StringBuilder;(I)Ljava/lang/StringBuildertoStringequals(Ljava/lang/Object;)Z! /*��!"
      #$        %& <x�Y�Y���L�:6�T�
�
 +�
�.4>EKPq▒���HK,'�!▒!f+,b-1_23[43 X567� 89:;;�V<=        >? u▒L*+��
                    "#&'"@323�;AB0
.J/                                                                                 
┌──(kali㉿kali)-[~/Documents/reversing/safer]
└─$ 
_____________________________________________________________________________
									FORMA 2
_____________________________________________________________________________
┌──(kali㉿kali)-[~/Documents/reversing/safer]
└─$ javac SafeOpener.class
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
error: invalid flag: SafeOpener.class
Usage: javac <options> <source files>
use --help for a list of possible options
                                                                            
┌──(kali㉿kali)-[~/Documents/reversing/safer]
└─$ 

┌──(kali㉿kali)-[~/Documents/reversing/safer]
└─$ file SafeOpener.class 
SafeOpener.class: compiled Java class data, version 52.0 (Java 1.8)
                                                                            
┌──(kali㉿kali)-[~/Documents/reversing/safer]
└─$ javap -classpath . -c SafeOpener 
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Compiled from "SafeOpener.java"
public class SafeOpener {
  public SafeOpener();
    Code:
       0: aload_0
       1: invokespecial #1                  // Method java/lang/Object."<init>":()V
       4: return

  public static void main(java.lang.String[]) throws java.io.IOException;
    Code:
       0: new           #2                  // class java/io/BufferedReader
       3: dup
       4: new           #3                  // class java/io/InputStreamReader
       7: dup
       8: getstatic     #4                  // Field java/lang/System.in:Ljava/io/InputStream;
      11: invokespecial #5                  // Method java/io/InputStreamReader."<init>":(Ljava/io/InputStream;)V
      14: invokespecial #6                  // Method java/io/BufferedReader."<init>":(Ljava/io/Reader;)V
      17: astore_1
      18: invokestatic  #7                  // Method java/util/Base64.getEncoder:()Ljava/util/Base64$Encoder;
      21: astore_2
      22: ldc           #8                  // String
      24: astore_3
      25: ldc           #8                  // String
      27: astore        4
      29: iconst_0
      30: istore        5
      32: iload         5
      34: iconst_3
      35: if_icmpge     119
      38: getstatic     #9                  // Field java/lang/System.out:Ljava/io/PrintStream;
      41: ldc           #10                 // String Enter password for the safe:
      43: invokevirtual #11                 // Method java/io/PrintStream.print:(Ljava/lang/String;)V
      46: aload_1
      47: invokevirtual #12                 // Method java/io/BufferedReader.readLine:()Ljava/lang/String;
      50: astore        4
      52: aload_2
      53: aload         4
      55: invokevirtual #13                 // Method java/lang/String.getBytes:()[B
      58: invokevirtual #14                 // Method java/util/Base64$Encoder.encodeToString:([B)Ljava/lang/String;
      61: astore_3
      62: getstatic     #9                  // Field java/lang/System.out:Ljava/io/PrintStream;
      65: aload_3
      66: invokevirtual #15                 // Method java/io/PrintStream.println:(Ljava/lang/String;)V
      69: aload_3
      70: invokestatic  #16                 // Method openSafe:(Ljava/lang/String;)Z
      73: istore        6
      75: iload         6
      77: ifne          119
      80: getstatic     #9                  // Field java/lang/System.out:Ljava/io/PrintStream;
      83: new           #17                 // class java/lang/StringBuilder
      86: dup
      87: invokespecial #18                 // Method java/lang/StringBuilder."<init>":()V
      90: ldc           #19                 // String You have
      92: invokevirtual #20                 // Method java/lang/StringBuilder.append:(Ljava/lang/String;)Ljava/lang/StringBuilder;
      95: iconst_2
      96: iload         5
      98: isub
      99: invokevirtual #21                 // Method java/lang/StringBuilder.append:(I)Ljava/lang/StringBuilder;
     102: ldc           #22                 // String  attempt(s) left
     104: invokevirtual #20                 // Method java/lang/StringBuilder.append:(Ljava/lang/String;)Ljava/lang/StringBuilder;
     107: invokevirtual #23                 // Method java/lang/StringBuilder.toString:()Ljava/lang/String;
     110: invokevirtual #15                 // Method java/io/PrintStream.println:(Ljava/lang/String;)V
     113: iinc          5, 1
     116: goto          32
     119: return

  public static boolean openSafe(java.lang.String);
    Code:
       0: ldc           #24                 // String picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}
       2: astore_1
       3: aload_0
       4: aload_1
       5: invokevirtual #25                 // Method java/lang/String.equals:(Ljava/lang/Object;)Z
       8: ifeq          21
      11: getstatic     #9                  // Field java/lang/System.out:Ljava/io/PrintStream;
      14: ldc           #26                 // String Sesame open
      16: invokevirtual #15                 // Method java/io/PrintStream.println:(Ljava/lang/String;)V
      19: iconst_1
      20: ireturn
      21: getstatic     #9                  // Field java/lang/System.out:Ljava/io/PrintStream;
      24: ldc           #27                 // String Password is incorrect\n
      26: invokevirtual #15                 // Method java/io/PrintStream.println:(Ljava/lang/String;)V
      29: iconst_0
      30: ireturn
}
```
## Bandera
picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}
## Notas adicionales
## Referencias
