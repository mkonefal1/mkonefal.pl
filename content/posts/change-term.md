+++
title = "Change the default terminal emulator in Ubuntu"
date = "2024-01-09"
description = "How to Change the Default Terminal Emulator in Ubuntu"
tags = [
    "terminal",
]
+++
1. Create symbolic link to x-terminal-emulator
```
sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator /PATH/TO/YOUR/TERMINAL 1
```

2.  Select your terminal to use as default
```
sudo update-alternatives --config x-terminal-emulator
```


###  Restore and remove the alternative link
```
sudo update-alternatives --remove x-terminal-emulator /PATH/TO/YOUR/TERMINAL
```

