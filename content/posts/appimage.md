---
title: "How to install Appimage apps"
date: 2024-01-25T02:33:41+01:00
---
AppImage is a format for distributing portable software on Linux without needing superuser permissions to install the application. It aims to provide a universal packaging format for all Linux distributions. Essentially, an AppImage is a self-contained package that contains an application and everything it needs to run that might not be present on each Linux system (like libraries and other dependencies).

One of the key features of AppImage is its simplicity: users just need to download a single AppImage file, make it executable, and run it. There's no need for unpacking or installation. This makes it incredibly user-friendly, especially for those who are new to Linux or prefer not to deal with the complexity of package managers.

AppImages are also system-agnostic. They should run across different Linux distributions without any modifications, making them ideal for software developers looking to distribute their applications to a broad Linux audience without having to package for multiple different distributions.

Another advantage of AppImage is that it doesn't affect the rest of the system. The application is isolated in its own package, reducing the risk of system libraries being altered or damaged. This makes AppImage a very safe method of software distribution and use.

Overall, AppImage is an innovative solution for software distribution in the Linux ecosystem, focusing on simplicity, portability, and ease of use.

## How to install

1. Make dir `appimage-apps` 
2. In `appimage-apps`  make dir with app name
3. Copy  .appimage file into that dir
4. `chmod 777 APPNAME.appimage`
5. Download png with icon and place it in same dir
6. Create file `APP-NAME.desktop`
7. Open that file in text editor and paste:

```
[Desktop Entry]
Name=YourApp
Exec=/path/to/app.AppImage
Icon=/path/to/nextcloud-icon.png
comment=app
Type=Application
Terminal=false
Encoding=UTF-8
Categories=Utility;
```
8. `chmod 777 APP_NAME.desktop`
8. `sudo cp /home/appimage-apps/APP-DIR/APP-NAME.desktop /usr/share/applications/`

