+++
title = "Installing tar.* apps"
date = "2024-01-09"
tags = ["linux", "Installing", "cli"]
+++
1. Copy .tar.* to /opt/
```
cd Downloads
sudo cp PROGRAM.TAR.* /opt/
```
2. Extract and remove compressed file
```
cd /opt/
sudo tar -xvf PROGRAM.TAR.*
sudo rm -rf PROGRAM.TAR.*
```
3. Change mode
```
sudo chmod 777 PROGRAM(EXTRACT)
```
4. To open apps in launcher create link to /usr/bin/
```
sudo ln -s /opt/PROGRAM(EXT)/ /usr/bin/PROGRAM-NAME
