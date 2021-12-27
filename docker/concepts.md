# VM vs Containers

| VM (house) | |
| ----- | ----- |
| Definition | Software that embeds a guest OS, kernel, lib/bin and application into a physical computer. Software called hypervisor manages all the VMs installed and communicates with the host OS and physical computer
| Pros | * Since it installs an entire guest OS per VM, it's possible to run for example a windows OS as a VM on a host computer that is built with mac OS\n * VMs can be more secure than containers because each VM can differ at the guess OS level\n * VMs have more resources available to them so could run more CPU / Memory intensive tasks  |
| Cons | * The more resources given means it takes up a lot of space on the physical computer |
| | * Since it installs an entire guest OS the start up time is longer than containers |
| | * Each guest OS needs to be updated and maintained separately |

---

| Container (apartment) | |   
| ----- | ----- |
| Definition | Software that embeds lib/bin and application into a physical computer. Software like docker daemon manages all the Containers installed and communicates with the host OS |
| Pros | * Lightweight (faster boot / less resource intensive) since it only installs applications and its bin/lib dependencies |  
| | * Easier to scale and move into different environments |
| Cons | * Relies on host OS. Cannot use applications or docker images that aren't compitible with underlying host OS |
| | * Weaker security boundaries because all containers within a computer operates on the same OS |

