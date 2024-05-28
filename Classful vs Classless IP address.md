CIDR vs Classful IP address 

 

CIDR (Classless Inter-Domain Routing)



CIDR allows IP addresses to be allocated and subnetted more flexibly than the older classful system. It uses a notation that combines the IP address and the subnet mask into a single string of numbers separated by a slash ("/").



#### Example 1: CIDR Notation



Consider the following CIDR notation:

- IP address: 192.168.1.0

- Subnet mask: 255.255.255.0



In CIDR notation, this is represented as:

- 192.168.1.0/24



Here, "/24" indicates that the first 24 bits of the IP address are the network portion, and the remaining 8 bits are for hosts. This allows for 2^8 (256) possible host addresses in this subnet.



#### Example 2: Variable-Length Subnet Mask



CIDR allows for variable-length subnet masks (VLSM), meaning you can subnet a network further into smaller subnets as needed. For instance:

- IP address: 10.0.0.0

- Subnet mask: 255.255.255.128



In CIDR notation, this becomes:

- 10.0.0.0/25



Here, "/25" means the subnet mask is 255.255.255.128, providing 2^7 (128) possible host addresses per subnet.



#### Benefits of CIDR:

- **Flexibility**: You can subnet and allocate IP addresses more efficiently.

- **Efficiency**: Reduces IP address wastage compared to classful addressing.

- **Scalability**: Facilitates easier internet routing and addressing management.





Classful IP Addresses (Older System)



Classful IP addressing divides IP addresses into fixed classes (A, B, C, D, E), each with predefined ranges and subnet masks. Here's how it worked:



#### Example 3: Classful IP Addressing



- **Class A**: 0.0.0.0 to 127.255.255.255

  - Subnet mask: 255.0.0.0 (8 bits for network)

  

- **Class B**: 128.0.0.0 to 191.255.255.255

  - Subnet mask: 255.255.0.0 (16 bits for network)

  

- **Class C**: 192.0.0.0 to 223.255.255.255

  - Subnet mask: 255.255.255.0 (24 bits for network)

  

- **Class D (Multicast)**: 224.0.0.0 to 239.255.255.255

  - No subnet masks specified, used for multicast addressing.

  

- **Class E (Reserved)**: 240.0.0.0 to 255.255.255.255

  - Reserved for future use, experimental purposes.



#### Limitations of Classful IP Addressing:

- **Wastage**: Often leads to inefficient use of IP addresses, especially in allocating large blocks to organizations that do not need them.

- **Rigid Subnetting**: Subnetting is fixed per class, making it less flexible compared to CIDR.



### Comparison Summary



CIDR's flexibility and efficient use of IP address space have made it the standard for internet addressing today. It allows for variable-length subnet masks, making subnetting more efficient and reducing address wastage. In contrast, classful addressing's fixed classes and subnetting rules were more rigid and less adaptable to the evolving needs of network management and internet growth.



In practical terms, CIDR notation is used extensively in network configurations and routing tables to specify how IP addresses are grouped and divided into smaller networks, enabling efficient internet traffic routing and management.
