# Linux commands

| Commands | Description |
| -------- | -------- |
| `cat /etc/issue` | Show distribution name of Linux and its version. [LINK](https://frontendmasters.com/courses/complete-intro-containers/chroot/) |
| `ldd PATH_TO_EXECUTABLE` | Show all dependencies of the executable like /bin/bash. [LINK](https://frontendmasters.com/courses/complete-intro-containers/chroot/) |
| `yes > dev/null` | Output 'y' into dev/null. This will use up CPU resources. |
| `yes \| tr \\n x \| head -c 1048576000 \| grep n` | Consume as much memory as it can |
