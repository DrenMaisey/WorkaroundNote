# What to do to free space on your windows PC

## Run Disk Cleanup
Choose to run also the System file cleanup


## Run this script to free the CBS logs folder

```batch
sc stop wuauserv
ping 127.0.0.1 -n 7 > NUL
cd \Windows\
move SoftwareDistribution SoftwareDistribution_old
del /S C:\Windows\Temp\* /Q
FOR /D %%p IN ("C:\Windows\Temp\*.*") DO rmdir "%%p" /s /q
sc start wuauserv
rd /S /Q C:\Windows\SoftwareDistribution_old
sc stop TrustedInstaller
ping 127.0.0.1 -n 7 > NUL
del /S C:\Windows\Logs\CBS* /Q
sc start TrustedInstaller
ping 127.0.0.1 -n 5 > NUL
wuauclt.exe /detectnow
```

## Run Patch Cleaner to free C:\windows\Install folder

[Download Patch Cleaner from the author site](http://www.homedev.com.au/Free/PatchCleaner "Download Patch Cleaner from the author site")


## Only for Windows 8.1 and up

From an elevated command promt

```batch
DISM.exe /online /Cleanup-Image /SpSuperseded
DISM.exe /online /Cleanup-Image /StartComponentCleanup
DISM.exe /online /Cleanup-Image /StartComponentCleanup /ResetBase
```