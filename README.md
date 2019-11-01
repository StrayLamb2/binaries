# binaries
My binary files, uploded to be moved easily, or for anyone that may need them.

git-auto: automated script to push changes on github

journal-cleaner: script to keep journal-size under control

merge-pdf: script to merge many files to a pdf

display-manager:  a script for sddm to correctly choose monitors (fixed sddm /w kscreen miscommunication)
                  the files in /usr/local/etc/ are just xrandr configuration files generated from arandr.
                  to use this script change the values of EXT_1, EXT_2, INT to your monitors, then create
                  the directory /usr/local/etc/display-manager, throw the xrandr configuration files inside
                  (using the correct names for each case) and run " sudo chmod +x /usr/local/etc/display-manager/* "
                  to make them executable. 
           
