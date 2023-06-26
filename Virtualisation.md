
![Alt text](<Diagram (1).JPG>)



**What is virtualisation?**

Virtualisation is a technology that allows you to create virtual versions of servers, storage, networks, and other physical machines. Using virtual software imitates the functions of actual hardware, enabling multiple virtual machines to run simultaneously on a single physical machine.

**What is a virtual machine?**

A virtual machine is a software-defined computer that runs on a physical computer with a separate operating system and computing resources. The physical computer is called the host machine, and virtual machines are guest machines. Multiple virtual machines can run on a single physical machine. Virtual machines are abstracted from the computer hardware by a hypervisor.


**Where can they be run?**

Virtual machines can be run on:

Desktop or laptop computers

Servers (both on-premises and cloud-based)

Cloud infrastructure provided by companies like AWS, Azure, and GCP

Specialised devices or appliances designed for virtualisation


**What determines how many can run?**

The number of virtual machines that can run on a system is determined by:

Physical resources available, such as CPU power, memory, storage, and network capacity.

Limitations or recommendations set by the virtualisation platform being used.

Resource requirements of each virtual machine based on the workload running inside it.

Efficient management and monitoring practices for maximising the number of virtual machines.

Scaling the hardware by adding more CPUs, increasing memory, or expanding storage.

**What does a virtual machine include?**

A virtual machine includes:

Virtual hardware: Virtualised components that imitate physical hardware, such as CPUs, memory, disks, and network interfaces.
Operating system: Each virtual machine runs its own separate operating system, like Windows, Linux, or macOS.

Applications and software: Virtual machines can host and run various software and applications, similar to a physical computer.

Virtualisation software: Also known as a hypervisor, it creates and manages the virtual environment, allowing the virtual machine to interact with the physical hardware.

Configuration and settings: Each virtual machine has its own specific settings, including resource allocations (CPU, memory), storage capacity, network settings, and other customisation options.


**What software is required to orchestrate/run the virtual machines?**

To orchestrate and run virtual machines, you need:

Hypervisor or Virtualization Platform: Core software that creates and manages virtual machines.

Virtual Machine Management Software: Tools to effectively manage virtual machines.

Operating System: Required for each virtual machine to run applications and software.

Virtual Machine Images: Pre-configured templates or snapshots of virtual machine setups.

Networking and Storage Infrastructure: Infrastructure for networking and storage needs of virtual machines


**What is the importance of an image when creating an VM?**

The importance of an image when creating a virtual machine (VM) includes:

Efficiency and time-saving: Using a pre-configured image saves time by quickly deploying a VM without starting from scratch.

Consistency and standardisation: Images ensure all VMs have the same baseline configuration, promoting uniformity.

Reproducibility: Images allow easy recreation of specific VM configurations, useful for development, testing, or production setups.

Security and stability: Trusted images undergo testing, updates, and security patches, enhancing VM security and stability.

Versioning and rollbacks: Images enable managing changes and reverting to previous configurations if needed.

https://aws.amazon.com/what-is/virtualization/#:~:text=Virtualization%20is%20technology%20that%20you,on%20a%20single%20physical%20machine.