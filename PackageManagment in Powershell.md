# Package Mmanager with Powershell

Required:
+ Powershell 5
+ internet connection

to do:
must verify if i need to install somethinf to use get-package

Open Powershell wih max privilege

get-packageprovider -name chocolatey

The provider 'chocolatey v2.8.5.130' is not installed.
chocolatey may be manually downloaded from https://oneget.org/ChocolateyPrototype-2.8.5.130.exe and installed.
Would you like PackageManagement to automatically download and install 'chocolatey' now?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):

put in Y and press enter

get-package  * chrome *



another way to do that is.

install-packageprovider -name chocolatey

It must be done within a console with maximun privilege 