## Software Development Process Stages: (Software Development Life Cycle - SDLC)
### 1. Requirement gathering and Analysis.
  Product features, users, usage, user requirement, market state.
### 2. Planning
  Cost, resources, and risk.
### 3. Design
  Detailed requirements and system design documents are created.
### 4. Software Development
  code is written by software developers.
### 5. Software Testing
  Defects are identified and tested for assurance.
### 6. Deployment
  Systems admins deploy for customer usage.
### 7. Maintenance and updating.

## SDLC Models:
### 1. Waterfall
  It is difficult to accommodate changes when not planned well. Cannot add new ideas.
### 2. Agile
  Covers the drawback of the waterfall model. Can be done in iterations of 2-4 weeks.
### 3. Spiral 
### 4. Big Bang, and so on.

## Continuous Integration:
  Code, Fetch, Build, Test, Notify, Feedback - it is a cyclic Process.
  The goal is to detect errors at an early stage so that they do not multiply. This helps fix it faster.
  IDE is integrated with version control to store and version the code.
  The Artifacts generated in this process are stored in software repositories for deployment and further testing.

## Continuous Deployment:
  Includes Server provisioning, dependencies, conf changes, network, artifact deploys, and so on.
  Decreases a lot of manual intervention and automates all the processes.
  
## Virtualization:
1. For running a single computer like multiple computers. VMWare allows this function.
2. Partition physical resources in virtual resources.
3. Virtual machines run in isolated environments.
4. The most common virtualization is server virtualization. Other Virtualizations include network, storage virtualization and so on.
5. Each VM needs its OS.

## Vagrant
It manages and automates the VM Lifecycle. It works on top of the Hypervisor.
1. We do not need OS installation. We have VM images/box. They are available on Vagrant Cloud.
2. We can manage all VM settings and make VM changes in a Vagrantfile.
3. Provisioning is available.
4. Simple to use.
5. **Some important commands:**
   a. vagrant up (to start the VM),
   b. vagrant destroy (to delete a VM),
   c. vagrant halt (to power off the VM),
   d. vagrant status(to see the status of the particular VM),
   e. vagrant global-status (to check the status of all VMs),
   f. vagrant box list (to list the available boxes on the computer).

## Terminologies known: Host OS, Guest OS, VM, Snapshot, Hypervisor.
Hypervisor types: Type 1: Bare metal and Type 2: runs as software on the computer.
HyperV from Microsoft is type 1.


