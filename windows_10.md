# Steps to optimize Windows 10 for better performance
- stay up to date
- uninstall unwanted programs
- scan with [malwarebytes](https://www.malwarebytes.com/)
- use SSD for C: partition (Windows OS)
- make sure C: has free space 5 GB as a minimum
- Power option -> high performance
- Settings > Privacy : disable them all
- Location : disable
- Background apps : disable except system ones
- Notification : disable
- Game bar : disable
- Game dvr : disable
- Broadcast - disable
- TruePlay - disable
- Defragment the C: to optimize
- Startup programs
- Win+R del temp
- Win+R del %temp%
- Del IDM downloaded
- Del recyclebin
- Disk cleanup
- Msconfig - disable services
- `advanced system settings` > `Performance Settings` > `Adjust for best performance`
- Settings > Personalization > Colors > OFF "Make Start, taskbar... transparent" and OFF others of your choice
- Settings > Ease of Access > Other options > OFF "Play animation" and OFF "Show background"
- Settings > Personalization > Start > Show more tiles OFF, Occasionaly show suggestions OFF
- Settings > Personalization > Lock screen > Get fun facts, tips, tricks > OFF (after previous point)
- HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\DataCollection\ AllowTelemetry: 0
- in powerShell (cmd)
```powershell
stop-service diagtrack
set-service diagtrack -startuptype disabled
```
- Store > user icon > Settings > Update apps automatically > OFF
- Store > user icon > Settings > Show products on tile > OFF
- regedit :
 - HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\WindowsStore Create a new 32-bit DWORD value named AutoDownload and set it to 2;
 - HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\CloudContent Create a new 32-bit DWORD value named DisableWindowsConsumerFeatures and set it to 1
- Disable [OneDrive](http://www.howtogeek.com/225973/how-to-disable-onedrive-and-remove-it-from-file-explorer-on-windows-10)
- Disable [Cortana](http://www.howtogeek.com/265027/how-to-disable-cortana-in-windows-10)
- Settings > System > Notifications & actions > Show me tips about Windows > OFF
- Settings > System > Offline maps > Automatically update maps > OFF
- Win + R > services.msc (for advanced users ONLY)
- optimize [Google Chrome](https://github.com/DevAbanoub/optimize_performance/blob/master/chrome.md)
- BIOS || UEFI > Enable virtualization and other CPU facilities
- BIOS || UEFI > Turn of power saving.
- fix filesystem errors : Win + R > cmd.exe > `CHKDSK C: /F`
- fix corrupted Windows files : Win + R > cmd.exe > `sfc /scannow`
- check HDD for bad sectors using __HD Tune__ or __HD Sentinel__

