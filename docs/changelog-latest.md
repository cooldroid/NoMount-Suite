**v1.3.216 — engine v36 (the engine fixes below need a kernel rebuild; the LKM zip carries them)**

- `apkscope`, `public.txt` and `accepted.list` survive a module update.
- `nm add|del --uid/--uid-range/--uid-excluded` reach the engine; the short form took the flags and served the rule to every uid.
- The bootloop guard arms before the engine module loads, honours `disabled`, and now counts a crash in the late reload pass.
- `nomount check` compares the bytes an app sees, not just the size, and stops reporting a canary it could not run as a kernel fault.
- A whiteout is refused on `/vendor_dlkm`, `/system_dlkm` and `/odm_dlkm`, and `whiteout add` refuses a path another module serves.
- Uninstalling removes its `nm` symlinks and no longer keeps `/data/adb/nomount` for good.
- WebUI: no "reflash your kernel" on an SELinux denial, no counts it could not read, no 100-second wait on a stale check request.
- Engine: the file and directory inode placers share one exclusion set, a synthesized directory is placed among its own siblings where there is room, and a rule under one is no longer freed with its children still pointing at it.

> `00_NoMount-Module` for a kernel with NoMount built in, `01_NoMount-Module-LKM` for one without.

```
ab9a085f7614806e50afa2adf0c802fc11e532a709689d57da0d5e717f8868a0  00_NoMount-Module-v1.3.216.zip
31ca69e5f448096001cb80ee3eaa7f19b62fb05e8e423ce37701a1458435782d  01_NoMount-Module-LKM-v1.3.216.zip
```
