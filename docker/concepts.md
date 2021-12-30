# VM vs Containers

| VM (house) | |
| ----- | ----- |
| Definition | Software that embeds a guest OS, kernel, lib/bin and application into a physical computer. Software called hypervisor manages all the VMs installed and communicates with the host OS and physical computer
| Pros | <ul><li>Since it installs an entire guest OS per VM, it's possible to run for example a windows OS as a VM on a host computer that is built with mac OS </li><li>VMs can be more secure than containers because each VM can differ at the guess OS level</li><li>VMs have more resources available to them so could run more CPU / Memory intensive tasks</li></ul> |
| Cons | <ul><li>The more resources given means it takes up a lot of space on the physical computer</li><li>Since it installs an entire guest OS the start up time is longer than containers</li><li>Each guest OS needs to be updated and maintained separately</li></ul> |

---

| Container (apartment) | |   
| ----- | ----- |
| Definition | Software that embeds lib/bin and application into a physical computer. Software like docker daemon manages all the Containers installed and communicates with the host OS |
| Pros |<ul><li>Lightweight (faster boot / less resource intensive) since it only installs applications and its bin/lib dependencies</li><li>Easier to scale and move into different environments</li></ul>|  
| Cons |<ul><li>Relies on host OS. Cannot use applications or docker images that aren't compitible with underlying host OS</li><li>Weaker security boundaries because all containers within a computer operates on the same OS</li></ul>|

---

# Open questions

1. How does linux-based docker image run on macOS?
ANS:
Seems like docker desktop has a built in [Linux](https://stackoverflow.com/questions/43383276/how-does-docker-run-a-linux-kernel-under-macos-host) [VM](https://stackoverflow.com/questions/66618003/why-is-it-possible-to-run-linux-containers-on-docker-in-macos). Also if you run `docker info` it will show the following output:

```
 Kernel Version: 5.10.76-linuxkit
 Operating System: Docker Desktop
 OSType: linux
 Architecture: aarch64
```

---

# Container parts

1. chroot - jail directories (file systems)
2. namespaces - jail processes / network / users etc (capabilities)
3. cgroups - jail cpu / memory etc (resources)

---

# Virtual Private Server

[VPSs](https://superuser.com/questions/1471167/whats-the-difference-between-vm-and-vps) are servers that you could rent from hosting companies. They could either be VMs or Containers.

# Resources

* [Link 1](https://www.youtube.com/watch?v=XCWWPpfdbsM)
* [Link 2](https://www.youtube.com/watch?v=5GanJdbHlAA)
* [Link 3](https://www.youtube.com/watch?v=9_s3h_GVzZc)
* [Link 4](https://www.youtube.com/watch?v=TvnZTi_gaNc)
* [Link 5](https://blog.engineyard.com/containers-vs-virtual-machines-differences-pros-cons)
* [Link 6](https://www.backblaze.com/blog/vm-vs-containers/)
* [Link 7](https://collabnix.com/how-docker-for-mac-works-under-the-hood/) (How docker works on mac)
* [Link 8](https://dev.to/lakhansamani/create-docker-image-on-apple-silicon-m1-mac-2f75) (Docker on M1 mac)
* [Link 9](https://frontendmasters.com/courses/complete-intro-containers) (Frontend masters course on Containers)
