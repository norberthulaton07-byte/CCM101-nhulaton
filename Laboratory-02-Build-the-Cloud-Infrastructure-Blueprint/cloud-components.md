## Compute Resources

Compute resources are the processing power that lets applications run and calculations get performed. In the cloud, this is delivered as virtual machines, containers, or serverless functions instead of dedicated hardware. This matters because it lets organizations scale processing power on demand, without buying and maintaining physical servers. This supports the elasticity that defines cloud computing. A Linux-based cloud terminal is itself a compute resource. It runs as a virtualized instance sharing physical hardware with other users. Each session gets a portion of CPU capacity, not a dedicated machine, similar to how AWS allocates virtual CPUs to instances.

## Storage Resources

Storage resources hold the OS files, application data, and user files a system needs. Cloud storage comes as object storage (backups, files), block storage (VM disks), or file storage (shared folders). This matters because it lets organizations expand capacity without buying physical drives, while gaining the redundancy providers build into their data centers. A Linux-based cloud environment relies on virtual disks from an underlying storage layer. This functions as block storage, reflecting how providers allocate disk space to instances without the user managing physical hardware.

## Networking Resources

Networking resources connect compute and storage to each other and to outside users. This includes IP addressing, virtual networks, firewalls, and gateways for secure communication. This matters because without networking, resources stay isolated and inaccessible; networking is what makes cloud services reachable over the internet. A Linux-based cloud instance is typically assigned an internal IP within a provider-managed virtual network. This mirrors how real cloud platforms assign machines an address inside a VPC or VNet to enable secure communication.

## Operating System

The operating system manages a machine's hardware, runs applications, and provides the interface users interact with, in this case a command-line shell. This is essential because the OS is the foundation every cloud workload runs on. Providers typically offer a choice of OS images so organizations can pick what fits their applications. Linux is commonly used as the base OS for cloud terminals because it's lightweight, open-source, and broadly supported. This is why it remains the dominant choice for cloud servers and virtualized environments.
