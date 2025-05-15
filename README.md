Why Docker Exist?
  
  Before Docker, we often ran into issues like:
  1. "It works on my machine" syndrome
  Code might work perfectly on a developer's computer but fail in testing or production due to different environments, library versions, or OS configurations.
  
  2. Complex setups
  Setting up a new environment could take hours or days — installing the right versions of Python, Node, databases, etc.
  
  3. Heavy virtual machines (VMs)
  VMs isolate apps well but are slow, large, and resource-hungry (they each need their own OS).
  
  4. Difficult deployment and scaling
  Moving apps from development to production was error-prone, inconsistent, and hard to automate.

Why Docker is lightwight?

  1. No Full Operating System in Each Container
   - VMs run a full OS inside each instance (including the kernel), which eats up CPU, RAM, and disk.
   - Docker containers share the host machine’s kernel and only include the minimal things needed to run the app (code + libraries).   
  ➡️ Less overhead. A Docker container might be just a few MBs, while a VM could be multiple GBs.

  2. Uses OS Features (Namespaces + Cgroups)
     Docker relies on built-in Linux features like:
       - Namespaces – isolate file systems, processes, users
       - Cgroups – control and limit resource usage (CPU, RAM)
  ➡️ It doesn’t need to "simulate" a machine like a hypervisor; it just isolates environments at the OS level.

How it slove the problems?
  1. Packaging with Docker Images
     A Docker image is like a blueprint for your application.
     It includes:
     a. Your code
     b. All dependencies (libraries, runtimes like Python/Node/Java)
     c. System tools or configs (if needed)
     This means:
     ➡️ You define everything your app needs in a file called a Dockerfile.
     ➡️ Docker builds a container image from that Dockerfile.

2. 

