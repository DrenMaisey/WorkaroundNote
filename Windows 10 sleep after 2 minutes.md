# Windows 10 sleeps after 2 minuts - workaround

1. Click on the windows icon
2. Type regedit
3. Right-click on regedit icon, click Run as administrator
4. Go to HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings\238C9FA8-0AAD-41ED-83F4-97BE242C8F20\7bc4a2f9-d8fc-4469-b07b-33eb785aaca0
5. Double click on Attributes
6. Enter number 2.
7. Go to Advanced power settings (click on Windows button, write power options, click on Power Options, in the selected plan click on the Change plan settings, click on the Change advanced power settings).
8. Click on the Change settings that are currently unavailable
9. Click Sleep, then System unattended sleep timeout, then change these settings from 2 Minutes to 20 for example.