**v1.3.219 — engine v36 · 1.36.8 ([engine]: rebuilt kernel or the 01_ zip)**

- [engine] overlay listings end like stock; SEEK_END on taken-over dirs = stat
- [engine] NOWAIT, O_DIRECT, DONTCACHE as stock
- [engine] SEEK_END locks, FIOQSIZE, FIONREAD: the caller's size
- [engine] inherited fds (zygote, providers): stock file for hidden apps
- [engine] hidden chmod/truncate: stock file
- [engine] inotify fhandle on overlay; generation on ext4/f2fs
- [engine] no injection into user-writable dirs; tmpfs dropped
- [engine] no ENOMEM listings during bulk adds
- [LKM] 6.12 loads on GKI again
- [LKM] 6.18 module
- [LKM] kept module survives same-KMI OTAs
- [LKM] overlay dir inodes numbered like stock
- [LKM] size guard: locks, FIOQSIZE, FIONREAD for hidden apps
- [LKM] ghost cloak: held fds answer fstat
- [LKM] load failures logged with the kernel's reason
- [Suite] crash-loop park (system_server x4 before boot)
- [Suite] two quick reboots no longer park
- [Suite] no late passes when the mount pass never ran
- [Suite] read-only OEM overlays counted
- [Suite] safe exports; hidden apps redacted from shared incident logs
- [Suite] ghost row: no false "not fully measured"
- [WebUI] engine offline vs unreachable; declined check falls back
- [WebUI] guard "not armed this boot"; crash-loop chip; last incident kept

> `00_NoMount-Module` for a kernel with NoMount built in, `01_NoMount-Module-LKM` for one without.

```
e5f16884bb00fdb60ce40332c331f2f4c329a2b8ce1b1fd9fe2a13e37598123d  00_NoMount-Module-v1.3.219.zip
2034bd850c5d53ca357ebc01ac3d53f4ec1fd16ce9c597121e32fbab143b0f9a  01_NoMount-Module-LKM-v1.3.219.zip
```
