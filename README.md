# IPFUnpacker
 - Usage : ipf_unpack.exe \<IPF file\> [decrypt/encrypt/extract]

#### "decrypt" feature
Decrypt feature will **replace** the encrypted IPF in argument by the decrypted one.  
Make sure to backup your IPF files somewhere before decrypting them.  
Make sure not decrypting twice the same IPF.  
Once decrypted, the IPF is readable by traditional tools (such as IPF Suite).  

#### "encrypt" feature
Encrypt will restore a decrypted IPF in argument to an encrypted one.  
Make sure not encrypting twice the same IPF.  

#### "extract" feature
Extract takes a decrypted IPF as argument and generates a list of files.
Some extension files aren't decrypted entirely ; In that case, only the MD5 of the decrypted is generated.

![HowTo](http://i.imgur.com/UJzXDZN.gif)


### Build the sources

If you want to build IPFUnpacker, I suggest using GCC - The code is compilable both under Windows and Linux.
Here is a quick guide how to compile the sources on Windows : 
- Download MSYS2 (http://sourceforge.net/projects/msys2/files/latest/download)
- Open the mingw64_shell.bat in the MSYS2 installation folder
- Launch the command "pacman -S gcc make zlib-devel"
- You should now be able to compile the code using "make clean && make release" next to the Makefile in the root folder.