# Group Policy Client Service can't start

## This problem could happen after some  windows update failure

1. Open RegEdit and navigate to HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services and verify if the key **Gpsvc** is present, if not there's notthing      to do, reinstall windows
2. Go to HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services verify if the _multistering_ value **GPSvcGroup** is present with the value **GPSvc** go to       the nest step otherwise create it.
3. in the same position of point (2) verify that the key **GPSvcGroup** is present and inside that is present the DWORD value **AuthenticationCapabilities**    with the value 0x00003020 (or 12320 decimal) and DWORD value  **CoInitializeSecurityParam** with value 0x00000001