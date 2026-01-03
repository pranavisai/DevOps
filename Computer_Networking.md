### Notes on Computer Networking

1. A computer network is communication between two or more network interfaces.
2. Components of a Computer Network:
   1. Two or more computers/devices.
   2. Cables as a link between the computers.
   3. A network interface card (NIC) on each.
   4. computer.
   5. switches.
   6. routers.
   7. software (OS).
3. OSI model: Standards set for worldwide data communication, so that systems are compatible with each other. ISO (International Organization of Standardization) has developed this standard.
4. OSI -> Open System Interconnection. Developed in 1984.
5. Seven-layer architecture in ascending order -> Physical, Data Link, Network, Transport, Session, Presentation, Application.
6. Basic elements of the model:
   1. Service(s) -> a set of actions that a layer offers to another layer.
   2. Protocol(s) -> a set of rules that a layer uses to exchange information.
   3. Interface(s) -> communication between the layers.
7. Classification of network by Geography:
   1. LAN -> Local area network.
   2. WAN -> Wide area network. (example: Internet)
   3. MAN -> Metropolitan area network. (example: metro trains)
   4. CAN -> Campus area network. (example: Intranet)
   5. PAN -> Personal area network. (example: hotstop, Bluetooth)
8. Switches -> Facilitates the sharing of resources by connecting all the devices together, including computers, printers, and servers.
9. Routers -> Receive and send data on computer networks. Can combine multiple networks together.
10. Public vs Private IP -> Public IP is for the internet, and Private IP is for the local network design.
11. Protocol(s) -> It is a formal specification that defines the procedures that must be followed when transmitting or receiving data. Format, timing, sequence, and error checking are defined.
12. TCP (Transmission Control Protocol) and UDP (User Datagram Protocol).
13. Networking commands Linux:
    1. ifconfig  or ip addr show -> shows active network interfaces, their names, and their ip addresses.
    2. ping <ip-addr> -> sends unlimited icmp packets till we stop. To check the connection with the machine.
    3. To add the name of the machine, go to /etc/hosts and add "ip-addr name". Then use the ping name.
    4. tracert <destination: example: www.google.in> -> to trace the complete route. It also checks the latency.
    5. netstat -antp or ss -tunlp -> to show all the TCP open ports.
    6. dig <website-name> or nslookup <website-name> -> shows DNS lookup.
    7. route -n -> To see the gateways.
    8. arp -> to view or add the content to the ARP table. A kernel maintains a table of all IP addresses or names and the mapping Mac address.
    9. mtr -> Same as tracert, but live. If the packet loss is frequent, we can run this command to check.
    10. telnet <ip-addr or host-name> -> to check if a particular port is open on the target machine or not.
