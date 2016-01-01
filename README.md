# MAME Build Tools

1. Download MSYS2. You can do that by downloading from http://msys2.github.io/ or
   from our mirror [for 64-bit Windows](https://github.com/mamedev/buildtools/releases/download/1.0/msys2-x86_64-20150916.exe) or [for 32-bit Windows](https://github.com/mamedev/buildtools/releases/download/1.0/msys2-i686-20150916.exe)
2. Run installation and let it finish and start command prompt, change default location by your needs
3. Update initial installation

   ```
   pacman --needed -Sy bash pacman pacman-mirrors msys2-runtime
   ```
4. Type exit to close current window and start "MSYS2 Shell" again
5. Now upgrade rest of packages

   ```
   pacman -Su
   ```
6. Install ConEmu console,make, wget and git tools

   ```
   pacman -S conemu-git make wget git
   ```
7. Go to top folder and download new startup batch file, and exit 

   ```
   cd /
   wget https://raw.githubusercontent.com/mamedev/buildtools/master/buildtools.bat
   exit
   ```
8. Start  ```buildtools.bat ``` from installed folder (by default it is C:\msys64 or c:\msys32)
9. Now it is time to install mingw and python

   For x64
   ```
   pacman -S mingw-w64-x86_64-gcc python
   ```

   For x86
   ```
   pacman -S mingw-w64-i686-gcc python
   ```

10. Download MAME source

   ```
   git clone https://github.com/mamedev/mame.git
   ```

# Update of packages

To update anytime in future just use:

   ```
   pacman -Su
   ```

# Optional packages

1. If you wish building SDL build you would need this :

   For x64
   ```
   pacman -S mingw-w64-x86_64-SDL2 mingw-w64-x86_64-SDL2_ttf
   ```

   For x86
   ```
   pacman -S mingw-w64-i686-SDL2 mingw-w64-i686-SDL2_ttf
   ```

2. If you wish building with QT5 debugger would need this :

   For x64
   ```
   pacman -S mingw-w64-x86_64-qt5
   ```

   For x86
   ```
   pacman -S mingw-w64-i686-qt5
   ```


2. To be able to generate documentation use:

   ```
   pacman -S doxygen 
   ```

3. To be able to use ccache to speed-up compiling 

   For x64
   ```
   pacman -S mingw-w64-x86_64-ccache 
   ```

   For x86
   ```
   pacman -S mingw-w64-i686-ccache 
   ```

4. Wish to compile with Clang, go ahead and download:
 
   For x64
   ```
   pacman -S mingw-w64-x86_64-clang mingw-w64-x86_64-clang-analyzer mingw-w64-x86_64-clang-tools-extra 
   ```

   For x86
   ```
   pacman -S mingw-w64-i686-clang mingw-w64-i686-clang-analyzer mingw-w64-i686-clang-tools-extra
   ```
