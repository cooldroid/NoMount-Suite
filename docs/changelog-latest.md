**v1.3.212 — engine v36 (needs a kernel rebuild)**

- Hide a rule from named apps: `nomount vfs add --uid-excluded <pkg,...>`. One entry covers that app under every user.
- `absorb` can do the same for an absorbed APK. Opt in with `/data/adb/nomount/apkscope`.
- A uid-scoped rule leaked to every uid once a permitted one looked it up. Legacy `--uid` too.

> `00_NoMount-Module` for a kernel with NoMount built in, `01_NoMount-Module-LKM` for one without.

```
b7d00340dc1cda8f89df82672700123bd2b4a108849cd8bc2493867e4eca782f  00_NoMount-Module-v1.3.212.zip
6ffeafe9434b8016e4cc374b2e4f1c450ec72b80955685f055010985217ec5ab  01_NoMount-Module-LKM-v1.3.212.zip
```
