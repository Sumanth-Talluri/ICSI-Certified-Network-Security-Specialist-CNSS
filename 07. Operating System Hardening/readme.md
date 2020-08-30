## Module 7 - Operating System Hardening

### Configuring Windows
- **Accounts, users, groups and passwords**
    - rename, disable default accounts.
    - **Administrator Accounts**
    - **Other Accounts**
    - IUSE_XXX
    - ASP.NET
    - Database accounts.
    - **Always use least privilege.**

- **Setting Security Policies**
    - individual machine policies.
    - secure password Policies
- **Account Lockout Policies**
- **Registry Settings**
    - contains critical info and settings for all HW/SW/users and prefrences.
    - stored in USER.DAT and SYSTEM.DAT (windows 95 and 98)
    - XP+ -> %SystemRoot%\System32\Config.
    - since Windows8 -> filename is ntuser.dat
    - use regedit32.exe/regedit.exe
    - has 5 main folders:
        - HKEY_CLASSES_ROOT - contains all file association types, OLE information and shortcut data.
        - HKEY_CURRENT_USER - links section of HKEY_USER for logged in user.
        - HKEY_LOCAL_MACHINE: computer specific info - hw/sw/other prefs.
        - HKEY_USER - individual prefs for each user of computer.
        - HKEY_CURRENT_CONFIG: links to section of HKEY_LOCAL_MACHINE - current hw config.
    - can alter registry keys.

- **Restrict Null Session Access**
    - can be exploited thorugh various shares.
    - is windows way of designating anonymous connections.
    - add **RestrictNullSessAccess** registry value -> 1 to all server pipes except **NullSessionPipes** and **NullSessionShares**.
    - **Key path**: HKLM\SYSTEM\CurrentControlSet\Services\LanmanServer.
- **Restrict Null Session Access Over Named Pipes**
   - HKLM\SYSTEM\CurrentControlSet\Services\LanmanServer.
   - delete all valutes.

- **Restrict Anonymous Access**
   - allows anonymous users to list domain usernames and enumerate share names.
   - HKLM\SYSTEM\CurrentControlSet\Control\Lsa
   - value 0-> allow anonymous Access, 1 -> restrict anonymous users, 2 -> Allow users with explicit anonymous perms.


- **Remote access to registry**
    - add key HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurePipeServers\winreg.
    - select winreg, cliet security -> clict permissions.
    - set  Administrator's perms to Full Control.
    - recommended value = 0

- **SErvices**
    - any not needed, should be shutdown.

- **Encrypting FS**
    - public key encryption, using CryptoAPI in win2k.

- **Security Templates**
    -  deploy these using GPO (Group policy objects)
    - stored in C:\Windows\Security\Templates.
    - Hisecdc.inf, Hisecws.inf, Securedc.inf, Securews.inf, Setup security.inf


### Configuring Linux
- nodev
- nosuid
- noexec
- find / -perm -4000
- find / -user root -perm -4000
- ro
- chroot


### OS Patches
- apply latest patches.



#### Continue on to [Module 8 - Virus Attacks and How to Defend](https://github.com/ArunNadda/CNSS/blob/master/Chapters/Module8-VirusAttacks-and-HowtoDefend.md)
