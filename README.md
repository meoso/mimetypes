What is does: Displays all system mime types and associated applications prefixed with the command `xdg-mime default`.

How to use it: 1) Execute the command and optionally pipe to grep searching for specific type or application. 2) copy and paste your choice of command.

Example 1: `./mimetypes | grep mp4`
may produce 
```
xdg-mime default ghb.desktop application/x-extension-mp4
xdg-mime default ghb.desktop audio/mp4
xdg-mime default ghb.desktop video/mp4
xdg-mime default ghb.desktop video/mp4v-es
xdg-mime default vlc.desktop video/mp4
xdg-mime default vlc.desktop video/mp4v-es
xdg-mime default vlc.desktop application/x-extension-mp4
xdg-mime default vlc.desktop audio/mp4
```
and i wish to set `vlc` as my default, so i copy/paste `xdg-mime default vlc.desktop video/mp4` to my shell prompt, thus setting `vlc` to open `mp4` mime-types.


Example 2: `/mimetypes.sh | grep html | grep firefox`
may produce 
```
xdg-mime default firefox.desktop text/html
xdg-mime default firefox.desktop application/xhtml+xml
```
and i wish to set Firefox as my default application for html mime-types, so i copy paste `xdg-mime default firefox.desktop text/html` into my shell prompt.

Thanks to "aleb" : http://unix.stackexchange.com/questions/36380/how-to-properly-and-easy-configure-xdg-open-without-any-enviroment
