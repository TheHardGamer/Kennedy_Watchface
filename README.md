# Kennedy Watchface

Watchface resembling the iconic watch worn by Leon S. Kennedy in requiem built using the watch face format for wearos 5 and above



## Building the .wfs Project File



Watch Face Studio expects a specific trailing binary signature (`normal\_watchface`) at the end of the zip archive. Standard archiving utilities strip this footer, causing an "Invalid Project" error. 



To properly pack the project tree, open PowerShell in the root directory and run:



```powershell

# Compress the source files into a zip archive
Compress all the folders and files into a zip using preferably WinRAR with compression set to store
Rename the file and change the extension from .zip to .wfs

# Append the required trailing verification string

Add-Content -Path .\Kennedy.wfs -Value "normal_watchface" -NoNewline

```



## Opening in Samsung Watch Face Studio



1. Copy the generated `Kennedy.wfs` file to your WFS workspace directory (typically `C:\\Users\\<YourUsername>\\WatchFaceStudio\\Workspace\\`).

2. Launch Watch Face Studio.

3. Select \*\*Open Project\*\* and choose `Kennedy.wfs`.



## Installing on the Watch



1. On your watch, go to \*\*Settings > Developer Options\*\*.

2. Enable \*\*ADB Debugging\*\*

3. Select your device from the list to build and deploy the project directly to the watch.



## Notes

1. It uses normal tick like effect for the seconds hand to keep the cpu usage as low as possible
2. The upper sub dial shows the current battery level (not pinpoint accurate, will fix later)
3. The bottom sub dial is empty as of now



## Preview



![Watchface Preview](latest\_preview.png)

