---
Title: gvm
Homepage: https://www.greenbone.net/
Repository: https://salsa.debian.org/pkg-security-team/gvm
Architectures: all
Version: 22.4.0+kali3
Metapackages: kali-linux-everything kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gvm
 
  The Greenbone Vulnerability Manager is a modular security auditing tool,
  used for testing remote systems for vulnerabilities that should be fixed.
   
  This package installs all the required packages. It provides scripts to setup,
  start and stop the GVM services.
   
  The tool was previously named OpenVAS.
 
 **Installed size:** `48 KB`  
 **How to install:** `sudo apt install gvm`  
 
 {{< spoiler "Dependencies:" >}}
 * gsad 
 * gvmd 
 * notus-scanner 
 * openvas-scanner 
 * ospd-openvas 
 * psmisc
 * rsync
 * xsltproc
 {{< /spoiler >}}
 
 ##### gvm-check-setup
 
 
 ```
 root@kali:~# gvm-check-setup -h
 gvm-check-setup 22.4.0
   Test completeness and readiness of GVM-22.4.0
 Step 1: Checking OpenVAS (Scanner)... 
         OK: OpenVAS Scanner is present in version 22.4.0.
         OK: Notus Scanner is present in version 22.4.1.
         OK: Server CA Certificate is present as /var/lib/gvm/CA/servercert.pem.
 Checking permissions of /var/lib/openvas/gnupg/*
         OK: _gvm owns all files in /var/lib/openvas/gnupg
         OK: redis-server is present.
         OK: scanner (db_address setting) is configured properly using the redis-server socket: /var/run/redis-openvas/redis-server.sock
         ERROR: redis-server is not running or not listening on socket: /var/run/redis-openvas/redis-server.sock
         FIX: You should start the redis-server with 'systemctl start redis-server@openvas.service' or configure it to listen on socket: /var/run/redis-openvas/redis-server.sock
 
  ERROR: Your GVM-22.4.0 installation is not yet complete!
 
 Please follow the instructions marked with FIX above and run this
 script again.
 
 ```
 
 - - -
 
 ##### gvm-feed-update
 
 
 ```
 root@kali:~# gvm-feed-update -h
 [>] Updating GVM feeds
 [*] Updating NVT (Network Vulnerability Tests feed from Greenbone Security Feed/Community Feed)
 ```
 
 - - -
 
 ##### gvm-setup
 
 
 ```
 root@kali:~# gvm-setup -h
 
 [>] Starting PostgreSQL service
 
 [>] Creating GVM's certificate files
 
 [>] Creating PostgreSQL database
 [i] User _gvm already exists in PostgreSQL
 [i] Database gvmd already exists in PostgreSQL
 [i] Role DBA already exists in PostgreSQL
 
 [*] Applying permissions
 GRANT ROLE
 [i] Extension uuid-ossp already exists for gvmd database
 [i] Extension pgcrypto already exists for gvmd database
 [i] Extension pg-gvm already exists for gvmd database
 [>] Migrating database
 [>] Checking for GVM admin user
 [*] Configure Feed Import Owner
 [>] Updating GVM feeds
 [*] Updating NVT (Network Vulnerability Tests feed from Greenbone Security Feed/Community Feed)
 ```
 
 - - -
 
 ##### gvm-start
 
 
 ```
 root@kali:~# gvm-start --help
 [i] GVM services are already running
 ```
 
 - - -
 
 ##### gvm-stop
 
 
 ```
 root@kali:~# gvm-stop -h
 [>] Stopping GVM services
 * gsad.service - Greenbone Security Assistant daemon (gsad)
      Loaded: loaded (/lib/systemd/system/gsad.service; disabled; preset: disabled)
      Active: inactive (dead)
        Docs: man:gsad(8)
              https://www.greenbone.net
 
 * gvmd.service - Greenbone Vulnerability Manager daemon (gvmd)
      Loaded: loaded (/lib/systemd/system/gvmd.service; disabled; preset: disabled)
      Active: inactive (dead)
        Docs: man:gvmd(8)
 
 Nov 24 04:58:38 kali systemd[1]: Starting Greenbone Vulnerability Manager daemon (gvmd)...
 Nov 24 04:58:38 kali systemd[1]: gvmd.service: Can't open PID file /run/gvmd/gvmd.pid (yet?) after start: Operation not permitted
 Nov 24 04:58:38 kali systemd[1]: Started Greenbone Vulnerability Manager daemon (gvmd).
 Nov 24 04:58:42 kali systemd[1]: Stopping Greenbone Vulnerability Manager daemon (gvmd)...
 Nov 24 04:58:42 kali systemd[1]: gvmd.service: Deactivated successfully.
 Nov 24 04:58:42 kali systemd[1]: Stopped Greenbone Vulnerability Manager daemon (gvmd).
 
 * ospd-openvas.service - OSPd Wrapper for the OpenVAS Scanner (ospd-openvas)
      Loaded: loaded (/lib/systemd/system/ospd-openvas.service; disabled; preset: disabled)
      Active: inactive (dead)
        Docs: man:ospd-openvas(8)
              man:openvas(8)
 
 Nov 24 04:58:37 kali systemd[1]: Starting OSPd Wrapper for the OpenVAS Scanner (ospd-openvas)...
 Nov 24 04:58:38 kali systemd[1]: Started OSPd Wrapper for the OpenVAS Scanner (ospd-openvas).
 Nov 24 04:58:42 kali systemd[1]: Stopping OSPd Wrapper for the OpenVAS Scanner (ospd-openvas)...
 Nov 24 04:58:43 kali systemd[1]: ospd-openvas.service: Deactivated successfully.
 Nov 24 04:58:43 kali systemd[1]: Stopped OSPd Wrapper for the OpenVAS Scanner (ospd-openvas).
 
 * notus-scanner.service - Notus Scanner
      Loaded: loaded (/lib/systemd/system/notus-scanner.service; disabled; preset: disabled)
      Active: inactive (dead)
        Docs: https://github.com/greenbone/notus-scanner
 
 Nov 24 04:58:38 kali notus-scanner[439849]:     raise AdvisoriesLoadingError(
 Nov 24 04:58:38 kali notus-scanner[439849]: notus.scanner.errors.AdvisoriesLoadingError: Can't load advisories. /var/lib/notus/products is not a directory.
 Nov 24 04:58:38 kali notus-scanner[439849]: Exception ignored in atexit callback: <function exit_cleanup at 0x7ffff5349870>
 Nov 24 04:58:38 kali notus-scanner[439849]: Traceback (most recent call last):
 Nov 24 04:58:38 kali notus-scanner[439849]:   File "/usr/lib/python3/dist-packages/notus/scanner/utils.py", line 112, in exit_cleanup
 Nov 24 04:58:38 kali notus-scanner[439849]:     sys.exit()
 Nov 24 04:58:38 kali notus-scanner[439849]: SystemExit:
 Nov 24 04:58:38 kali systemd[1]: notus-scanner.service: Can't open PID file /run/notus-scanner/notus-scanner.pid (yet?) after start: Operation not permitted
 Nov 24 04:58:42 kali systemd[1]: notus-scanner.service: Deactivated successfully.
 Nov 24 04:58:42 kali systemd[1]: Stopped Notus Scanner.
 ```
 
 - - -
 
 ### openvas
 
  The tool OpenVAS has been renamed Greenbone Vulnerability Manager (GVM).
   
  This is a transitional package that pulls the new gvm, it can be safely
  removed once gvm has been installed.
 
 **Installed size:** `11 KB`  
 **How to install:** `sudo apt install openvas`  
 
 {{< spoiler "Dependencies:" >}}
 * gvm
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

![gvm](images/openvas.png)

## OpenVAS Usage Examples

Before trying to do anything with OpenVAS, you must first run the setup script, appropriately named `openvas-setup`. At the end of the (very long) setup process, the automatically created password will be displayed to you. **Save the password somewhere safe**.

```
root@kali:~# openvas-setup
ERROR: Directory for keys (/var/lib/openvas/private/CA) not found!
ERROR: Directory for certificates (/var/lib/openvas/CA) not found!
ERROR: CA key not found in /var/lib/openvas/private/CA/cakey.pem
ERROR: CA certificate not found in /var/lib/openvas/CA/cacert.pem
ERROR: CA certificate failed verification, see /tmp/tmp.YpvirUZgxc/openvas-manage-certs.log for details. Aborting.

ERROR: Your OpenVAS certificate infrastructure did NOT pass validation.
       See messages above for details.
Generated private key in /tmp/tmp.XwwD8IOl5u/cakey.pem.
Generated self signed certificate in /tmp/tmp.XwwD8IOl5u/cacert.pem.
Installed private key to /var/lib/openvas/private/CA/cakey.pem.
Installed certificate to /var/lib/openvas/CA/cacert.pem.
Generated private key in /tmp/tmp.XwwD8IOl5u/serverkey.pem.
Generated certificate request in /tmp/tmp.XwwD8IOl5u/serverrequest.pem.
[...]
znc_detect.nasl
znc_detect.nasl.asc
zone_alarm_local_dos.nasl
zone_alarm_local_dos.nasl.asc
OpenVAS community feed server - http://www.openvas.org/
This service is hosted by Greenbone Networks - http://www.greenbone.net/

All transactions are logged.

If you have any questions, please use the OpenVAS mailing lists
or the OpenVAS IRC chat. See http://www.openvas.org/ for details.

By using this service you agree to our terms and conditions.

Only one sync per time, otherwise the source ip will be blocked.

receiving incremental file list
./
COPYING
          1,493 100%    1.42MB/s    0:00:00 (xfr#1, to-chk=84/86)
COPYING.asc
            181 100%  176.76kB/s    0:00:00 (xfr#2, to-chk=83/86)
nvdcve-2.0-2002.xml

...

sha1sums
          2,002 100%    2.34kB/s    0:00:00 (xfr#33, to-chk=2/36)
timestamp
             13 100%    0.02kB/s    0:00:00 (xfr#34, to-chk=1/36)
timestamp.asc
            181 100%    0.21kB/s    0:00:00 (xfr#35, to-chk=0/36)

sent 719 bytes  received 41,272,464 bytes  398,774.71 bytes/sec
total size is 41,260,051  speedup is 1.00
/usr/sbin/openvasmd
User created with password 'xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxx'.
```

After the setup completes, you will find two listening TCP ports: 9390 and 9392. Port 9392 is likely the one of most interest to you as it is the web interface for OpenVAS. You can open the web interface using your browser of choice.

```
root@kali:~# ss -lnt4
State      Recv-Q Send-Q Local Address:Port               Peer Address:Port
LISTEN     0      128     127.0.0.1:9390                        *:*
LISTEN     0      128     127.0.0.1:9392                        *:*

root@kali:~# firefox https://127.0.0.1:9392
```

Despite reminding people to save the default password generated during setup, it still sometimes gets misplaced. Fortunately, the “openvasmd” utility can be used to create and remove users as well as reset their passwords.

```
root@kali:~# openvasmd --create-user=dookie
User created with password 'yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyy'.
root@kali:~# openvasmd --get-users
admin
dookie
root@kali:~# openvasmd --user=dookie --new-password=s3cr3t
root@kali:~# openvasmd --user=admin --new-password=sup3rs3cr3t
```

OpenVAS signatures can be updated with the “openvas-feed-update” utility.

```
root@kali:~# openvas-feed-update
Updating OpenVas Feeds
OpenVAS community feed server - http://www.openvas.org/
This service is hosted by Greenbone Networks - http://www.greenbone.net/

All transactions are logged.

If you have any questions, please use the OpenVAS mailing lists
or the OpenVAS IRC chat. See http://www.openvas.org/ for details.
[...]
```

Verify the certificates that are configured for OpenVAS.

```
root@kali:~# openvas-manage-certs -V
OK: Directory for keys (/var/lib/openvas/private/CA) exists.
OK: Directory for certificates (/var/lib/openvas/CA) exists.
OK: CA key found in /var/lib/openvas/private/CA/cakey.pem
OK: CA certificate found in /var/lib/openvas/CA/cacert.pem
OK: CA certificate verified.
OK: Certificate /var/lib/openvas/CA/servercert.pem verified.
OK: Certificate /var/lib/openvas/CA/clientcert.pem verified.

OK: Your OpenVAS certificate infrastructure passed validation.
```
