# Mac commands

| Commands | Description | 
| ------- | ------- |
| `system_profiler SPSoftwareDataType` | Show apple hardware and software config. [LINK](https://www.cyberciti.biz/faq/mac-osx-find-tell-operating-system-version-from-bash-prompt/) |
| `uname -av` | Show OS X darwin kernel version. [LINK](https://www.cyberciti.biz/faq/mac-osx-find-tell-operating-system-version-from-bash-prompt/) | 
| `otools -L PATH_TO_EXECUTBLE` | Show all dependencies of an executable like /bin/bash. [LINK](https://discussions.apple.com/thread/309193) |
| `file PATH_TO_EXECUTABLE` | Shows if an executable is supported on x86_64 and/or arm64e architecture. Example `file /usr/bin/mandoc`. For some reason mandoc only includes [support](https://apple.stackexchange.com/questions/430310/apple-silicon-usr-bin-mandoc-bad-cpu-type-in-executable) for x86_64 on the m1 mac |
