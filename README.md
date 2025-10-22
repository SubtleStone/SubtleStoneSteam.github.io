# STEAM FIXES


## Description
___
Below are the problems and fixes, I have encountered so far.


## TABLE OF FIXES
___

INDEX |
---------|
PROCESSING SHADERS TAKES  TOO LONG




### 1. *PROCESSING SHADERS TAKES TOO LONG*
___

Shaders were taking 30-40 mins to process. So, I started looking for a fix and found this solution on reddit.


"

   Open your **File Manager**, if you are new to Linux you can just open a terminal and type Dolphin, Thunar, Nemo whatever your file manager is.
   Press **Ctrl+H** to see hidden files.

Go to
> .local/share/steam  (Here you should see other folders like appcache, bin, clientui, compatibilitytools.d, config etc


If you use a flatpak version

Go to
   > .var/app/com.valvesoftware.Steam/data/Steam
   
 
 
 Create a file called steam_dev.cfg
 Open the file with any text editor and add
> unShaderBackgroundProcessingThreads X

where X is the number of cores for your cpu if you have hyperthreading
For example if you are using i9,13900k your threads is 32.
If you are using Ryzen 5 4600 you have 12 threads.



Faster shader pre-compilation
In certain circumstances shader pre-compilation may only use one core, however this can be overridden by the user, example to use 8 cores:

> ~/.steam/steam/steam_dev.cfg

> unShaderBackgroundProcessingThreads 8 

"
***

- [X]  Fix for me that worked for me :
   
   - // in my case it is 6 cores. Since my processor is Intel i5 10h. It seems to work but the difference isn't massive in my case ( Skyrim ).


- [X] Source

 - [steamcommunity](https://steamcommunity.com/discussions/forum/1/4423184732111747107/).

 - [archlinuxwiki](https://wiki.archlinux.org/title/Steam/).         

      
