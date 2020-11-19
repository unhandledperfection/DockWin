
# DockWin
Script to quickly save / restore all opened window size and positions (for Windows OS).

![System Tray](https://raw.github.com/unhandledperfection/DockWin/master/docs/images/ss_icon_tray.png)

## Table of contents
* [General Info](#general-info)
* [Setup](#setup)
* [Usage](#usage)
* [Command Line Usage](#command-line-usage)
* [Technologies](#technologies)
* [Development](#development)
* [Releases](#releases)
* [Origins](#origins)

## General info
* Upon running DockWin, an icon will appear in your system tray. This icon facilitates the common operations such as `save windows positions` or `restore windows positions`.
* After performing the save operation, DockWin will generate a config file `WinPos.txt` in the same directory as the executable.

example of generated WinPos.txt:
```
SECTION: Monitors=2,MonitorPrimary=1; Desktop size:0,0,4480,1440
Title="Sublime Text",x=-8,y=-8,width=2576,height=1416,maximized=1,path=""
Title="sshsession@server:Default",x=3520,y=18,width=960,height=1062,maximized=0,path=""
```

## Usage
1. Open a powershell terminal
2. Download the executable (note to compile from source see the Development section.)
```
Invoke-WebRequest -Uri "https://github.com/unhandledperfection/DockWin/releases/download/v0.8.0/DockWin.exe" -OutFile "DockWin.exe"
```
3. Run Dockwin
```
.\Dockwin.exe
```
4. Save current window positions by pressing **[Win]+0**

From here on you can now restore window positions using **[Win]+[Shift]+0**

## Command Line Usage
* Restore using default config file
```
DockWin.exe /restore
```
* Restore using specific config file
```
DockWin.exe /restore C:\Path\To\Your\WinPos.txt
```

## Technologies
* AutoHotkey


## Development
1. Install AutoHotkey from https://autohotkey.com/
2. Open a terminal (cmd or powershell) and cd into this repo directory
3. Compile an executable from the source
```
& 'C:\Program Files\AutoHotkey\Compiler\Ahk2Exe.exe' /in .\DockWin.ahk /out .\DockWin.exe
```
4. Run the executable
```
.\DockWin.exe
```

## Origins
https://autohotkey.com/board/topic/112113-dockwin-storerecall-window-positions/page-3