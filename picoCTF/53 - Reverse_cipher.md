# Reverse_cipher
## Descripcipción
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this). Can you reverse the flag.
## Pistas
- objdump and Gihdra are some tools that could assist with this
## Solucion
```
┌──(kali㉿kali)-[~/Documents/reversing/rever]
└─$ file rev     
rev: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=523d51973c11197605c76f84d4afb0fe9e59338c, not stripped
┌──(kali㉿kali)-[~/Documents/reversing/rever]
└─$  file rev_this 
rev_this: ASCII text, with no line terminators
┌──(kali㉿kali)-[~/Documents/reversing/rever]
└─$ cat rev_this
picoCTF{w1{1wq85jc=2i0<}                                                                            
┌──(kali㉿kali)-[~/Documents/reversing/rever]
└─$ 
-----------------------------------------------------------------------------
							MODIFICADO CON GHINDRA
-----------------------------------------------------------------------------
void main(void)

{
  size_t sVar1;
  char flag [23];
  char local_41;
  int local_2c;
  FILE *flagrev;
  FILE *flagfile;
  uint j;
  int i;
  char rev;
  
  flagfile = fopen("flag.txt","r");
  flagrev = fopen("rev_this","a");
  if (flagfile == (FILE *)0x0) {
    puts("No flag found, please make sure this is run on the server");
  }
  if (flagrev == (FILE *)0x0) {
    puts("please run this on the server");
  }
  sVar1 = fread(flag,0x18,1,flagfile);
  local_2c = (int)sVar1;
  if ((int)sVar1 < 1) {
                    /* WARNING: Subroutine does not return */
    exit(0);
  }
  for (i = 0; i < 8; i = i + 1) {
    rev = flag[i];
    fputc((int)rev,flagrev);
  }
  for (j = 8; (int)j < 0x17; j = j + 1) {
    if ((j & 1) == 0) {
      rev = flag[(int)j] + '\x05';
    }
    else {
      rev = flag[(int)j] + -2;
    }
    fputc((int)rev,flagrev);
  }
  rev = local_41;
  fputc((int)local_41,flagrev);
  fclose(flagrev);
  fclose(flagfile);
  return;
}

-----------------------------------------------------------------------------
									PHYTON
-----------------------------------------------------------------------------
  GNU nano 7.2                                                                     exp.py                                                                              
cifrado = open('rev_this','r').read()
print(cifrado)

flag = ''

for i in range(8, len(cifrado)-1):
        if i & 1 == 0:
                flag += chr( ord(cifrado[i]) - 5) 
        else:
                flag += chr( ord(cifrado[i]) + 2)
print(flag)
```
## Bandera
picoCTF{w1{1wq85jc=2i0<}
r3v3rs37ee84d27
picoCTF{r3v3rs37ee84d27}
## Notas adicionales
- Instalar ghindra
## Referencias
- https://www.intel.com/content/dam/develop/external/us/en/documents/introduction-to-x64-assembly-181178.pdf
- https://ghidra-sre.org/
