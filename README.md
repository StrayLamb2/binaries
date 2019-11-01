# binaries
My binary files, uploded to be moved easily, or for anyone that may need them.

### git-auto 
automated script to push changes on github

### journal-cleaner
script to keep journal-size under control

### merge-pdf 
script to merge many files to a pdf

### display-manager  
Change the variables to your specific setup:
- **EXT_1**  
	Main external monitor
- **EXT_2**  
	Secondary external monitor
- **INT**    
	Laptop monitor (or otherwise the default/fallback monitor)

Create the directory for the scripts:
```
sudo mkdir -p /usr/local/etc/display-manager
```

Create your scripts, suitung your needs (easiest way is arandr):
```
arandr
```
and save them using the following names:
- **dual_external**  
	The setup to run when all screens are connected
- **single_external**  
	The setup to run when a single external monitor is connected
- **internal**  
	The setup where no external monitors are connected / Fallback mode

Copy your scripts in the directory:
```
sudo cp "DIRECTORY_CONTAINING_YOUR_SCRIPTS"/* /usr/local/etc/display-manager/*
```

Make them executable:
```
sudo chmod +x /usr/local/etc/*
```

Tell SDDM to run this script:
```
sudo cat > /usr/share/sddm/scripts/Xsetup <<EOF
#!/bin/sh
/usr/local/bin/display-manager
EOF
```
