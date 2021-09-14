
# Table of Contents

1.  [Dotfiles](#org658aecb)
2.  [Games](#orgdeb71d2)
    1.  [Morrowind](#orge0e19c2)
        1.  [Installing MGE XE](#org9b083b5)



<a id="org658aecb"></a>

# Dotfiles

List of repositories hosting my dotfiles for Linux

-   [Dotfiles](https://github.com/ArtemSmaznov/Dotfiles)
-   [qTile](https://github.com/ArtemSmaznov/qTile)
-   [AwesomeWM](https://github.com/ArtemSmaznov/AwesomeWM)
-   [Vim](https://github.com/ArtemSmaznov/Vim)
-   [dmscripts](https://github.com/ArtemSmaznov/dmscripts)
-   [Wallpapers](https://github.com/ArtemSmaznov/Wallpapers)


<a id="orgdeb71d2"></a>

# Games


<a id="orge0e19c2"></a>

## Morrowind

-   [Morrowind Graphics Guide](https://wiki.nexusmods.com/index.php/Morrowind_graphics_guide)
    -   [MGE XE](https://www.nexusmods.com/morrowind/mods/41102)
    -   [Morrowind Code Patch](https://www.nexusmods.com/morrowind/mods/19510/)
-   [House in Balmora](https://www.nexusmods.com/morrowind/mods/43209?tab=files&file_id=1000002739)


<a id="org9b083b5"></a>

### Installing MGE XE

[reddit: Morrowind + MGE XE Mod (Wine Or Proton)](https://www.reddit.com/r/linux_gaming/comments/e78v9a/morrowind_mge_xe_mod_wine_or_proton/)

1.  Install Morrowind
2.  Get the Wine/Proton prefix directory
    
    If you installed Morrowind using the `Steam` client
    
        /home/USERNAME/.steam/steam/steamapps/compatdata/22320/pfx/
    
    If you installed Morrowind using something like `PlayOnLinux`
    
        /home/USERNAME/PlayOnLinux's virtual drives/Morrowind/
3.  Launch the terminal and enter the following commands
    
        WINEPREFIX="/path/to/wine/prefix" winecfg
4.  Go to the Libraries tab
5.  Add the `dinput.dll` and `d3d8.dll` and set the added DLLs to &ldquo;native, builtin&rdquo;
6.  Click Apply and then click OK
7.  Install `Winetricks`
8.  Launch the terminal and enter the following commands
    
        WINEPREFIX="/path/to/wine/prefix" winetricks d3dcompiler_43
        WINEPREFIX="/path/to/wine/prefix" winetricks d3dcompiler_47
        WINEPREFIX="/path/to/wine/prefix" winetricks d3dx9_43
9.  Install MGE XE mod
    
        env WINEPREFIX="/PATH/TO/WINE/PREFIX" wine "C:\windows\command\start.exe" /Unix "/PATH/TO/MGE.exe"

