# Introduce

written by **sunus Lee**

<sunuslee@gmail.com>

_this software is licensed by MIT License._

This "Backup Box" is a script that let your cloud storage like dropbox/google driver/yunio,etc to back/sync
any file in your machines, so that you don't have to manually copy those file to the **local cloud storage directory(e.g ~/Dropbox)**

# Installation

1. Use one of the methods to get the script.
   * download directly `wget https://raw.github.com/sunuslee/bub/master/bub`
   * `git clone https://github.com/sunuslee/bub.git`

2. Configure the cloud root directory path.
   1. open the file **bub**
   2. change the **CLOUD_DRIVER_ROOT** to your local cloud storage directory path.
       * normally, the local cloud storage directory is in your $HOME.
       * that directory will be sync by the cloud storage itself, **not bub**
       * examples:
          
                #dropbox
                CLOUD_DRIVER_ROOT="/Users/sunus/Dropbox/MacBook"
                #yunio
                CLOUD_DRIVER_ROOT="/Users/sunus/Youio/MacBook"

   3. give bub executeable premission.
           
           chmod +x bub 
   
   4. save the changes and copy hub to your $PATH, eg(/usr/bin)
        
          sudo cp bub /usr/bin

# Usage
    after the installation.
    
    Usage: bub option path1 path2 ...
    options:
    -s Use to selete custome file/directories. 
       do not copy the full path and parent directory
    -i Normal Dropbox mode, just copy to Dropbox directory. same as cp
    -h Show this help and exit
    
    one of options -s or -i must be present.
