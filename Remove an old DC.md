# Remove an old and crashed DC

There are certain situations however, such as server crash or failure of DCPROMO option, that would require a manual removal
of the DC from the system by cleaning up the servers metadata.

## Remove from Domain Controller
1. Log in to DC server as Domain/Enterprise administrator and navigate to **Server Manager > Tools > Active Directory Users and Computers**

2. Expand **Domain > Domain Controllers**

3. Right click on the DC server that need to remove manually and click **delete**

4. In next dialog box, click yes to confirm

5. In next dialog box, select **This Domain Controller is permanently offline and can no longer be demoted using the Active Directory Domain Services Installation Wizard (DCPROMO)** and
   click **Delete**
6. if the domain controller is global catalog server, in next window click **yes** to continue with deletion

7. If the domain controller holds any FSMO roles in next window, click **ok** to move them to the domain controller which is available   


## Remove from Site and services

Go to **Server manager > Tools > Active Directory Sites and Services**

1. Expand the Sites and go to the server  which need to remove
2. Right click and click **Delete**
3. In next window click **yes** to confirm

## Remove from DNS
Go to DNS and remove the deleted server object records


## Test AD and Replication

Form eleveted Powershell
1. dcdiag
2. REPADMIN /SHOWREPL